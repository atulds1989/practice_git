#this is readme file to practice git version controll system the flow if from local to remote

If we are working from remote to local then flow:

1. create a repositary in github/gitlab
2. create folder in local
3. clone the repo from remote to the local folder by -- git clone <link of the repo created in github>
4. configure the local with the remote (this step is neccessary)
 - git config --global user.name "user name of the github profile"
 - git config --global user.email "email by you have created the github profile"
 - git config --list (to check the configuration detail you have entered)
 - git remote add origin <url of repository>
5. made the changes in the existing files or create new files.
6. git add . (add the files to the staging area)
7. git commit -m "...name the commit you can write the brief of your changes"
8. git push origin Main (Main is your branch name)
    ----here is some important commands regarding branches
    - git branch (to see the current branch)
    - git branch -m <new name for the branch by default it is master>
    - git checkout <branch name> (to checkout from current branch to the another branch.pass the branch name where to go)
    - git checkout -b <newbranchname> ( to create the new branch)
    - git branch -d <branchname> ( to delete the branch)
    - to set the upstream for the push command we can try this
      - git push origin Main -U
9. merge:
    - git diff <branchname> (to check wheter there is any difference in the branches or not)
    - git merge <branchname> (to merge the current branch working on to the branch with which you want to merge your code)
    
## to catch the changes from remote to local
10. git pull origin Main (Main is the working branch name it can be anything you had given to your branch)
    --- merge conflict
    - if some one is working on the same code and he made changes prior to you and pushed then when you push your change then the bash will through error that first pull code from remote to local
    - if some one is working on the same function and doing same kins ==d of change like addition of three numbers but different variable names then when we push to the remote it says to pull first and when we pull then it will through an error named merge conflict . it can be resolved by mutual understandig of developers.

11. .gitignore file:
    --- .gitignore file can be created from vs code or github remote repositary
    - it is very useful to not to push the files folders on remote just by placing their names into this file


