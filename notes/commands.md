# Git Commands

HEAD always refers to the last commit on a branch.

`git config --global user.name  "Adam Snetiker"` <br>
Configure Git username

`git config --global user.email "ajsnetiker@gmail.com"` <br>
Configure Git email address

`git config --global core.editor "mate -w" <br>
Configure default text editor

`git config --global --list` <br>
List global configuration settings

`git config --global -e` <br>
Open configuration file with the default editor

`mate <file-name>` <br>
Open TextMate 2

`git init <repository-name>` <br>
Start a fresh project with no existing source code 

`git init ` <br>
Add a new repository to an existing project folder

`git clone https://github.com/username/repository-name.git` <br>
Clone a repository to make a full copy on your local system

`git status` <br>
See if there are any changes between working directory, local repository, and remote repository

`git add <file-name>` <br>
Adds a file to the stage to be committed

`git add -A` <br>
Adds and update any changes to the working directory, including renames and deletions. Use after making changes outside of Git.

`git reset HEAD <file>` <br>
Remove file from the stage so it won't be committed

`git rm --cached <file>` <br>
Remove file from the stage so it won't be committed

`git push origin master` <br>
Push file to the remote repository on GitHub

`git pull origin master` <br>
Pull down any changes from the remote repository to local repository. It's practice to always do a pull before doing a push  to make sure everything is in sync.

`git commit` <br>
Commit a file and open text editor to write a single or multi-line message

`git commit -m "Put inline commit message here"` <br>
Commit a file and include a one-line message in the terminal

`git commit -am "Commit message here."` <br>
Use -a to add any changes that have been made and commit them with an inline message. Only use when you're making a straightforward change to a single file.

`git ls-files` <br>
Lists all files that are being tracked in the repository. Above command only works on these files.

**Fork (on GitHub)**  <br>
Make a copy of a repository into your personal account. Do this before cloning the repository.

`git add .` <br>
Recursively add files to the repository. Add many files at once from multiple directory levels.

`git reset HEAD <file-name>` <br>
Cancel changes and remove file from the staging area

`git checkout <file-name>` <br>
Get back to the state of files as they were last committed

`git mv <current-file-name> <new file-name>` <br>
Rename a file

`git rm` <br>
Remove files that are already being tracked by git. Use Bash version of rm to delete the file.

`git checkout -- <file-name>` <br>
Discard changes in the working directory

`git help <command>` <br>
Show help for a specific command

`git log` <br>
Show commit history in reverse chronological order (most recent first)
	- SHA1 hash
	- Author
	- Date

`git log --abbrev-commit` <br>
Show history with shorter commit IDs

`git log --oneline --graph --decorate` <br>
Compress entries into one line.
Show an ASCII branching graph
Use labels and colors to annotate different parts of the commit results

`git log --file` <br>
Show commits involving a particular file

`git log --follow -- path/to/file` <br>
Show all history including renames

`git show <commit-ID>`  <br>
Show history using a particular commit ID

`git config --global alias.hist "log --all --graph --decorate --oneline"` <br>
Create an alias called hist for a long command

`git hist` <br>
New command using the alias created above

`mate ~/.gitconfig` <br>
Open the gitconfig file to add more settings. You can modify settings or add more aliases to the file.

`mate .gitignore` <br>
Ignore unwanted files and folders so they're never tracked, added, or committed to a repository.  <br>
One expression per line. Name of file, name of folder, or pattern.
	* access.log
	* *.log
	* logs/

`git reflog` <br>
Show a log of everything we've done

`git reset <commit-ID>` <br>
Got to a particular commit in the log
