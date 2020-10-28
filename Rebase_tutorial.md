# Branching and Rebase tutorial

## Step 1: Create a new local branch  
`git branch <new_branch_name>`
`git switch <new_branch_name>`

OR

`git checkout -b <new_branch_name>`

## Step 2: Pushing the local branch to remote branch
`git push -u origin rebase_example`

## Step 3: Rebasing previous commits  
`git rebase -i HEAD~3` (The number of commits that you want to change)

##### Options:  
- Pick: Change the order
- Reword: Edit the commit message
- Squash: Combine two commits while retaining both the commit messages
- Fixup: Combine two commits but keeping only the first commit message
- Edit: Edit an existing file or add a new one. This is followed by `git commit --amend` for each commit and then once all changes are finished run `git rebase --continue`