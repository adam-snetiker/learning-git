# Tagging

Use  tags to label significant changes or milestones in a repository.

`git tag <tag-name>` <br>
Create a lightweight tag

`git tag --list` <br>
List all tags

`git show <tag-name>` <br>
Show all commits labeled with the specified tag

`git tag --delete <tag-name>` <br>
Delete the specified tag

`git tag -a <tag-name>` <br>
Add extra information to create an annotated tag, similar to a commit message. It's common to use a version number such as v-1.0 as the tag name. When using the -a flag, the default editor will come up. Enter a relevant message.

`git commit --amend` <br>
Allows you to edit your commit message

`git tag <tag-name> -m "Tag message here"` <br>
Amend a tag annotation without opening the text editor

`git diff <tag-name-1> <tag-name-2)` <br>
`git difftool <tag-name-1><tag-name-2)` <br>
Compare the difference between multiple tags.

`git tag -a <tag-name> <commit-ID>` <br>
Tag a specific commit based on its ID.

`git tag -a <tag-name> -f <commit-ID>` <br>
Update a tag for a specific commit.

`git push origin <tag-name>` <br>
Look for differences and push a tag to GitHub. All commits associated with the specified tag are pushed also.

`git push origin <branch-name> --tags` <br>
Synchronize master branch and push all tags to GitHub at once.

`git push origin :<tag-name>` <br>
Delete a tag from GitHub. This would be used when you don't want to make certain things public, such as alpha releases.
