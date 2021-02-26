# Comparing, Branching, and Merging

P4Merge  -  perforce.com

P4Merge Configuration (in root directory)

**Set as Diff tool**
`git config --global diff.tool p4merge`
`git config --global difftool.p4mergepath /Applications/p4merge.app/Contents/MacOS`
`git config --global difftool.prompt false`

**Set as Merge Tool**
`git config --global merge.tool p4merge`
`git config --global mergetool.p4mergepath` /Applications/p4merge.app/Contents/MacOS`
`git config --global mergetool.prompt false`

## Comparisons

`git diff`
Compare  the staging area to the working directory.

`git difftool`
Open the diff tool set in config and show a visual view.

`git diff HEAD`
git difftool HEAD
Compare the working directory to the last known commit to the Git repository
HEAD is the last known commit on the branch

`git diff --staged HEAD`
git difftool --staged HEAD
Compare the staging area to the last known commit

`git diff -- path/to/file`
git difftool -- path/to/file
Limit comparisons to one file or path

`git diff <commit-ID1> <commit-ID2>`
Compare changes between commits
One of them could be head
Find IDs using git log --oneline

`git diff HEAD HEAD^ `
`git difftool HEAD HEAD^ `
^ is the second to last commit
^1 is used to go back more than one level

`git diff master origin/master`
Compare between local and remote master branches
Specify which is on the left and which one the right

## Branching
`git branch -a`
List all local and remote branches

`git branch <branch-name>`
Create a new branch

`git checkout <branch-name>`
Switch branches

`git checkout -b <branch-name>`
Create a new branch with -b flag, then switch to that branch automatically

`git branch -m <old-branch-name> <new-branch-name>`
Rename a branch 
-m is for move

`git branch -d <branch-name>`
Delete a branch using -d flag. Use -D for force delete.

## Merging
`git checkout master`
Move to the master branch using 

`git diff master title-change`
Show the differences between branches

`git merge <source-branch-name>`
Merge the source branch into the master branch

** Fast Forward Merge **
A merge made when there are no changes being made on the target branch. No additional work was done on the Master branch before merging.

`git merge --no-ff `
Disable fast forwarding merges

`git merge <branch-name> -m "Commit message here."`
Merge a branch and preserve simple-changes as a separate branch. Auto merge will succeed if there are no conflicts.

** Resolving Merge Conflicts **
A conflict occurs when changes are made to the same file on different branches. If you make a change on one branch and switch back to the other, the changes won't be reflected in that file if the branches aren't merged. GIt automatically manages the working directory for you.

Git marks up the file to show conflicts.

`<<<<<<<< HEAD`
Shows changes made on the master branch

`>>>>>>>> other-branch`
Shows changes made on other branches

`git mergetool`
Use the graphical merge tool to resolve conflicts visually

Use arrows to navigate between conflicts. Press the colored shape label to the right of each line to choose which version of that change should be correct. Each colored shape label corresponds to a different change. Once changes are resolved, commit again. When out of the merge conflict, git status will show Master instead of Master | Merging.

When you make changes, Git will track all version of changes in temp files. To avoid merging those, add *.orig to the .gitignore file.
