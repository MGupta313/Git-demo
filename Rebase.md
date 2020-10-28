# Changing Multiple Commit Messages

To modify a commit that is farther back in your history, you can use the rebase tool.

With the interactive rebase tool, you can then stop after each commit you want to modify and change the message, add files, or do whatever you wish.

For example, if you want to change the last three commit messages you use:  
`git rebase -i HEAD~3`

It opens the last three commit messages in a text editor for you to change:

pick 64a30fd Update Fetch_merge_example.txt
pick 20f5828 Create Creating_New_Branch.md
pick 1d6367e Rename GoToCommands.md to Go_To_Commands.md

![rebase.png](https://github.com/MGupta313/Git-demo/blob/main/rebase.png)
