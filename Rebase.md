# Changing Multiple Commit Messages

To modify a commit that is farther back in your history, you can use the rebase tool.

## Git Rebase

The `git rebase` command allows you to easily change a series of commits, modifying the history of your repository. You can reorder, edit, or squash commits together.

Basically, rebase = change.

### Uses:  
- Edit previous commit messages  
- Combine multiple commits into one  
- Delete or revert commits that are no longer necessary  


With the interactive rebase tool, you can then stop after each commit you want to modify and change the message, add files, or do whatever you wish.

For example, if you want to change the last three commit messages you use:  
`git rebase -i HEAD~3`

It opens the last three commit messages in a text editor for you to change:

pick 64a30fd Update Fetch_merge_example.txt
pick 20f5828 Create Creating_New_Branch.md
pick 1d6367e Rename GoToCommands.md to Go_To_Commands.md

![rebase.png](https://github.com/MGupta313/Git-demo/blob/main/rebase.png)

There are five commands available while rebasing:

1. **Pick**  
It means that a particular commit is included. If you change the order of pick commands, the order of commits changes when rebase is running. If you want to delete a particular commit, you can just delete the pick command line of that commit in the opened file.

2. **Reword**  
If you have made a typo or want to change the commit message altogether, you can use reword which pauses the rebase process and gives you a chance to change the commit message.

3. **Edit**  
If you want to make changes to your commit like editing any file in your project or you want to add a file to your commit, you can use edit which stops the process and gives you a chance to amend changes. For each change you make, you'll need to perform a new commit, and you can do that by entering:  
`git commit --amend`  
When you're finished making all your changes, you can run  
`git rebase --continue`

This also allows you to split a large commit into smaller ones, or, remove erroneous changes made in a commit.

4. **Squash**  
If you want to combine two or more commits into a single one, you can use squash which also lets you write a new commit describing both the changes.

This operation requires your input so it opens the text editor and asks you to write "first commit message" and "second commit message" and then save it. This makes any changes you want in the commit messages.

5. **Fixup**  
If you want to simply merge a commit to a previously made commit, use fixup. It merges the changes from 2nd commit to 1st one and discards the 2nd commit's message and simply retains the 1st commit's message.

_Detailed explanation with examples of these commands can be found here:_ [Git Rebase Command Line](https://docs.github.com/en/free-pro-team@latest/github/using-git/using-git-rebase-on-the-command-line)

**NOTE:** The commits you chose to rebase are sorted in the order of the oldest changes (at the top) to the newest changes (at the bottom).

#### Resolving merge conflicts after a Git rebase

When you perform a git rebase operation, you're typically moving commits around. Because of this, you might get into a situation where a merge conflict is introduced. That means that two of your commits modified the same line in the same file, and Git doesn't know which change to apply.

- You can run `git rebase --abort` to completely undo the rebase. Git will return you to your branch's state as it was before git rebase was called.  
- You can run `git rebase --skip` to completely skip the commit. That means that none of the changes introduced by the problematic commit will be included. It is very rare that you would choose this option.  
- You can fix the conflict. [How to resolve a merge conflict](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line)


