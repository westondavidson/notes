# ASP.NET Core (.NET Framework)
# Build and test ASP.NET Core projects targeting the full .NET Framework.
# Add steps that publish symbols, save build artifacts, and more:
# https://docs.microsoft.com/azure/devops/pipelines/languages/dotnet-core

trigger:
- main

pool:
  vmImage: 'windows-latest'

variables:
# change to wherever solution file actually is
# I think this is already pointing to the correct location
  solution: '**/*.sln'
  buildPlatform: 'Any CPU'
  buildConfiguration: 'Release'
steps:
- task: SonarCloudPrepare@1
  inputs:
    SonarCloud: 'sonarcloud'
    organization: '210215-usf-net'
    scannerMode: 'MSBuild'
    projectKey: '210215-USF-NET_Weston_Davidson-P1'
    projectName: 'Weston_Davidson-P1'




- task: DotNetCoreCLI@2
  inputs:
    command: 'build'
    projects: $(solution)

- task: DotNetCoreCLI@2
  inputs:
    command: 'test'
    projects: '**/StoreTests/*.csproj'
    arguments: --configuration $(buildConfiguration) --collect "Code Coverage"
- task: PublishCodeCoverageResults@1
  inputs:
    codeCoverageTool: 'Cobertura'
    summaryFileLocation: '**/coburtura/coverage.xml'
- task: SonarCloudAnalyze@1
  displayName: public code analysis

- task: SonarCloudPublish@1


- task: DotNetCoreCLI@2
  inputs:
    command: 'publish'
    publishWebProjects: true
    zipAfterPublish: true


- task: AzureRmWebAppDeployment@4
  inputs:
    ConnectionType: 'AzureRM'
    azureSubscription: 'connectionforproject'
    appType: 'webApp'
    WebAppName: 'sineshop1'
    packageForLinux: '$(System.DefaultWorkingDirectory)/**/*.zip'