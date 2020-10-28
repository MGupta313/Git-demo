# Basics of Github/Git

## Step1: Cloning a repo  
`git clone  <clone_repo_url>`

## Step2: Making changes in the local copy of the repo  
Add any file or make changes to a current file or delete a file

## Step3: Transferring those changes from the local copy to the remote repo  
`git add .`  
`git commit -m "<commit_message>"`  
`git push origin <branch_name>`

Repeat these steps every time you make any changes to any of the files in your local copy of the repo.

#### Dealing with "non-fast-forward" errors  
If your local copy of a repository is out of sync with, or "behind," the upstream repository you're pushing to, you'll get a message saying non-fast-forward updates were rejected.  
This means that you must retrieve, or "fetch," the upstream changes, before you are able to push your local changes.  

Example: If another person has pushed to the same branch as you, Git won't be able to push your changes.

`git fetch origin`  
(This gets or fetches all the changes made to the online/remote repo.)  
`git merge origin YOUR_BRANCH_NAME`  
( This merges updates made online with your local copy.)

Or just use git pull  
`git pull origin YOUR_BRANCH_NAME`  
(This grabs online updates and merges them with your local copy.)