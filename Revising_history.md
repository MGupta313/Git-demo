# Revising history

Many times, when working with Git, you may want to revise your local commit history.

## Changing the Last Commit  
Changing your most recent commit is probably the most common rewriting of history that you’ll do.  
You’ll often want to do two basic things to your last commit: simply _change the commit message_, or change the actual content of the commit by _adding, removing and modifying files._

`git commit --amend`

This opens the commit message in a text editor where you can change the meesage, save and exit.

If you want to the content of the file of your last commit, make the changes, stage those changes and then do `git commit --amend`. This replaces the last commit with the improved and changed commit.

**NOTE: Don’t amend your last commit if you’ve already pushed it.**