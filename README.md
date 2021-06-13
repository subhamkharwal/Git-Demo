# Git-Demo
This Repo is for Git Demo

## Git Basic Operation commands

 - `git init` To start a new git repo
 - `git branch` To check the current branch
 - `git add .` To add all modified files to Stage
 - `git add <file name>` To add a specific file to Stage
 - `git status` To check the changes on the branch and to check the *staged* files
 - `git commit -m "<Your comment for Commit>"` To commit changes to local repo
 - `git branch <branch name>` To create a new branch
 - `git checkout <branch name>` To select a particular branch
 - `git checkout master` To checkout master branch
 - `git merge <branch name>` To merge branch to master branch
 - `git remote add origin <repository url>` To add a remote github repo account to publish changes
 - `git push -u origin master` To push the changes to remote Git repo
 - `git pull origin <branch name>` To pull the branch from remote branch to local repo
 
 
 
## Issue with `git push` 
 
We have sometimes encountered a situation where the `git push -u origin master` or the `git push` command to remote repository is stuck for very long.
To resolve the issue:
- Try debugging the using the below command
```
GIT_TRACE=1 git push -v origin master
```
- If the error is with credential manager same as below screenshot, try un-installing the credential manger `git credential-manager uninstall`
- ![image](https://user-images.githubusercontent.com/85821447/121806639-4d488800-cc6e-11eb-80a6-c9dfaee276d2.png)
- Once done, try pushing you changes again. This time you will be prompted again for username and password.
- Enter the correct credentials and Done.
