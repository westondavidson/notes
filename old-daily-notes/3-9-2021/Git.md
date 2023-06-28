# git!
- git is a distributed version control system
- git has features that let you work on multiple versions of a project at the same time
- you have your main branch, and then other branches that branch off, sometimes you can accidentially have multiple "true" branches
- you want to make sure you have one single standardized branch that everyone can pull from. need to pull from main branch to ensure that any other branches still have the "truth" involved

# branching
- best practice to have a different branch for any new features you want to add to the working project
- use git checkout -b branch-name to create a new branch pulled from the main
- git push pushes current branch
- git pull origin branch-name lets you pull from a specific branch 
    - pretty much just want to pull from main to avoid weird other branch bugs

# branching terminology
- remote branch - branch in remote repository
- local branch - branch in local repo
- tracking branch
    - upstream branch
    - local branch with a direct relationship to a remote branch

# pull requests
- don't just push to main
- when you want to merge a completed feature to the main branch, create a pull request
- a pull request opens any changes you want to commit to main for peer review
- any changes you've made on the branch will be added to the pull request

# merge conflicts
- when two people try to merge by changing file stuff at the same place, git will get mad and ask you to manually review
- we pull often and push often to avoid merge conflicts
- don't work on the same branch as another person!!

- https://dangitgit.com/
- good for figuring out how to solve small issues that have occurred during git branch/commit/push processes

- fast forward merge:
    - when you don't have any merge conflicts
- non fast forward
    - when there's conflictss