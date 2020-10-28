# Branches

## Listing remote branches  
`git branch -r`

## Listing all branches (local and remote)  
`git branch -a`

## Delete a branch locally  
`git branch -d <branch_name`

## Delete a branch remotely  
`git push <remote> --delete <branch_name>` (eg. git push origin --delete test_branch)

## Copying a branch
`git branch -c [<oldbranch>] <newbranch>`

## Pushing a local branch to remote  
`git push (-u|--set-upstream) origin <branchname>`