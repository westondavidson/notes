- we'll be building a pipeline for the toh app
- we'll come across multiple errors - I'm gonna take notes on them lol
- ci/cd pipelines


- use boards for p2



steps:
- task: DotNetCoreCLI@2
  inputs:
    command: 'build'
    projects: '**/*.sln'

- task: DotNetCoreCLI@2
  inputs:
    command: 'test'
    projects: '**/StoreTests/*.csproj'

- task: DotNetCoreCLI@2
  inputs:
    command: 'publish'
    publishWebProjects: true
    workingDirectory: 'Weston_Davidson-P1'


NEED TO MAKE PIPELINE PRIVATE WTF?????
---------------------

steps:
- task: DotNetCoreCLI@2
  inputs:
    command: 'build'
    projects: '**/*.sln'

- task: DotNetCoreCLI@2
  inputs:
    command: 'test'
    projects: '**/StoreTests/*.csproj'

- task: DotNetCoreCLI@2
  inputs:
    command: 'publish'
    publishWebProjects: false
    zipAfterPublish: true
    projects: '**/StoreMVC/*.csproj'


- task: AzureRmWebAppDeployment@4
  inputs:
    ConnectionType: 'AzureRM'
    azureSubscription: 'Azure subscription 1(0bcf3285-b43d-4285-97f2-47f2ef104e66)'
    appType: 'webApp'
    WebAppName: 'sineshop'
    packageForLinux: '$(System.DefaultWorkingDirectory)/**/*.zip'





# issues that occurred
- in a newly created devops account, only private projects can be deployed for default build agents
- 




weston-davidson71430
westondavidoson@outlook.com


08b1d311ed56d6c54b9350a86845eb10cf22d2ef




--------------------------



- I WILL NEED TO GO BACK AND MAKE SURE I HAVE CODE COVERAGE DONE CORRECTLY
- rewatch lecture from 3-11-2021 to see how to add tests and code coverage to yml file
- then deploy pipeline again
- it should be near the end of the video
- cobertura for code coverage tool
- summary file is in **/coburtura/coverage.xml