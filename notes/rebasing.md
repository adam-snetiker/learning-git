# Rebasing

Rebasing means incorporating any changes made on the master branch to other branches, whereas merge means the opposite.

Rewind the change that happened on the second branch
* Play back the change from master
* Re-apply the change that was made on the feature branch the first time.

Change to the branch you want to rebase into: <br>
`git rebase master`

Rebasing conflicts occur when there are conflicting changes between the master branch and another branch. Open the merge tool with `git mergetool` and choose which version of conflicting changes you want. Once problems are fixed, you can move forward.

`git rebase --abort` <br>
Abort a rebase

`git rebase --continue` <br>
Continue a rebase after resolving all conflicts

`git fetch` <br>
Non-destructive command that updates references between local repository and remote repository

`git pull --rebase origin master` <br>
Keep local changes ahead of the changes on GitHub, but get the benefit of all changes that have been made on there.
