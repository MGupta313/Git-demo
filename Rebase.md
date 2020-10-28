# Changing Multiple Commit Messages

To modify a commit that is farther back in your history, you can use the rebase tool.

With the interactive rebase tool, you can then stop after each commit you want to modify and change the message, add files, or do whatever you wish.

For example, if you want to change the last three commit messages you use:  
`git rebase -i HEAD~3`

It opens the last three commit messages in a text editor for you to change:

pick 64a30fd Update Fetch_merge_example.txt
pick 20f5828 Create Creating_New_Branch.md
pick 1d6367e Rename GoToCommands.md to Go_To_Commands.md

# Rebase 7fded00..1d6367e onto 7fded00 (3 commands)
#
# Commands:
# p, pick <commit> = use commit
# r, reword <commit> = use commit, but edit the commit message
# e, edit <commit> = use commit, but stop for amending
# s, squash <commit> = use commit, but meld into previous commit
# f, fixup <commit> = like "squash", but discard this commit's log message
# x, exec <command> = run command (the rest of the line) using shell
# b, break = stop here (continue rebase later with 'git rebase --continue')
# d, drop <commit> = remove commit
# l, label <label> = label current HEAD with a name
# t, reset <label> = reset HEAD to a label
# m, merge [-C <commit> | -c <commit>] <label> [# <oneline>]
# .       create a merge commit using the original merge commit's
# .       message (or the oneline, if no original merge commit was
# .       specified). Use -c <commit> to reword the commit message.
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.




