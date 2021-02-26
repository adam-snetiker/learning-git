# Stashing

`git stash`
Save changes that are a work-in-progress without committing. Invokes the save command by default. Title goes back to what it was if you stash a file and reopen it. Useful when you want to make changes to a different file. Does not stash untracked files.

Use stash when the platform you're using definitely enforces having a clean working directory.

`git stash apply`
Retrieve saved file from the stash.

`git stash list``
Shows all stashes and messages. Last stash is index 0.

`git stash drop`
Drop files in the last stash when you no longer need them to be saved.

`git stash -u``
Include untracked files that are not being excluded by .gitignore

`git stash pop`
Apply changes from the stash and drop the stash

`git stash save "like a commit message but for a stash, used to differentiate stashes"``

`git stash save "another message to create another stash"`

`git stash show stash@{#}`
reflog syntax that shows files changed in a particular stash

`git stash apply stash@{#}`
Apply the change in the specified stash.

`git stash drop stash@{#}`
Drop changes in the specified stash

`git stash branch <branch-name>`
Create a new branch and apply stash to that branch.