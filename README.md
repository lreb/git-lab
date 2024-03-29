# git-lab

# ** Status ** 

This project was generated with to give solutions to all users that need IT solution in Jabil.

[![Website shields.io](https://img.shields.io/website-up-down-green-red/http/shields.io.svg)](http://shields.io/)
[![Generic badge](https://img.shields.io/badge/version-1.0.0-green.svg)](https://shields.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)

----------
## How to configure the tooling commands
The below command will set the name of your commit transactions.
$ git config –global user.name “[name]”
The below command will set the email to your commit transactions.
$ git config –global user.email “[email address]”
How to create Repositories
The below command will create a new repository with a specified name.
$ git init [project-name]
The below command will allow you to download a project and its complete version.
$ git clone [url]
How to refactor the file name
The below command will delete the file from the working directory and stages the deletion.
$ git rm [file]
The below command will allow you to delta the file from the version control but saves it locally.
$ $ git rm –cached [file]
The below command will change the file name and prepare it for commit.
$ git mv [file-original] [file-renamed]

## How to suppress the tracking
The below command will list all the ignored files within the project.
$ git ls-files –others –ignored –exclude-standard
How to shelve and restore incomplete changes
The below command will temporarily store all the modified tracked files.
$ git stash
The below command will restore the most recently stashed file.
$ git stash pop
The below command will list all the stashed changesets.
$ git stash list
The below command will discard the most recently stashed changeset.
$ git stash drop
## Commands to erase mistakes
The below command will undo all the commits but preserve the changes locally.
$ git reset [commit]
The below command will discard all the history and changes back to the specific commit.
$ git reset –hard [commit]
## Commands for group changes
The below command will display all the local branches in the current repository.
$ git branch
The below command will allow you to create a new branch.
$ git branch [branch-name]
The below command will delete the specified branch.
$ git branch -d [branch-name]

## Miscellaneous commands
The below command will allow you to connect your local repository to the remote server.
$ git remote add [variable name] [Remote Server Link]

## To Split a subfolder out in a new repository.
$ git filter-branch --prune-empty --subdirectory-filter master
To remove untracked files
$ git clean -f

## To remove untracked files/directories
$ git clean -fd

## list all files/directories that would be removed
$ git clean -nfd

## The below command will tar the project files without .git directory.
$ tar cJf .tar.xz / --exclude-vcs

## several commands

![alt text](https://nvie.com/img/git-model@2x.png)

## GIT tricks

### Add .gitignore

`touch .gitignore`

### Initialize repository

`git init`

### Add files or folders

`git add .`

`git add mypath/here`

`git add mypath/here/myfile.cs`

### commit changes

`git commit -m "my awesome changes"`

`git commit -am "I dont care anything and I am going commit all"`

### Get changes

`git pull`

`git pull origin mybranch`

### Push changes

`git push`

`git push origin mybranch`

### List branch

`git branch`

`git branch -r`

### Create branch

`git checkout -b mynewbranch`

### Push branch change to remote server

git push --set-upstream <origin_name> <branch_name>


### Switch branch

`git checkout mybranch`

### Merge branch

`git merge my_branch_with_changes` (before switch to target branch)

### Delete branch

Delete locally branch

`git branch -d branch_name`

Force to delete brench unmerged

`git branch -D branch_name`

### Untrack folder from git

Permanently ignore changes to a file

`git rm -r --cached Applications\CTOSuiteAPI\CTOSuite.Data.Access\obj\`

Resume tracking files with:

`git update-index --assume-unchanged <file>`

`git update-index --no-assume-unchanged <file>`

rm is the remove command
-r will allow recursive removal
–cached will only remove files from the index. Your files will still be there.
The . indicates that all files will be untracked. You can untrack a specific file with git rm --cached foo.txt

## Undo all uncommitted or unsaved changes
this will unstage all files you might have staged with git add:

`git reset`
This will revert all local uncommitted changes (should be executed in repo root):

`git checkout .` 
You can also revert uncommitted changes only to particular file or directory:

`git reset --hard HEAD`
This will remove all local untracked files, so only git tracked files remain:

`git clean -fdx`
WARNING: -x will also remove all ignored files, including ones specified by .gitignore! You may want to use -n for preview of files to be deleted.

git reset --hard # removes staged and working directory changes

read comments and manual.

git clean -f -d
remove untracked

git clean -f -x -d 
CAUTION: as above but removes ignored files like config.

git clean -fxd :/ 
CAUTION: as above, but cleans untracked and ignored files through the entire repo (without :/, the operation affects only the current directory)

### Revert file to previous commit version
`git checkout [some_dir|file.txt]`
Yet another way to revert all uncommitted changes (longer to type, but works from any subdirectory):
 
`git checkout <commit_number> -- dir1\dir2\myfile.cs`

or

`git checkout origin/<branch_name> -- dir1\dir2\myfile.cs`

then just add this file again with `git add dir1/dir2/myfile.cs`, commit your changes and push your commits

### view remote url

`git remote -v`

### Add remote url

`git remote add origin <ssh-url>`

### Remove remote url

`git remote rm origin or <origin name>`

### Releases & Version Tags

Show all released versions

`git tag`

Show all released versions with comments

`git tag -l -n1`

Create release version

`git tag v1.0.0`

Create release version with comment

`git tag -a v1.0.0 -m 'Message'`

Checkout a specific release version 

`git checkout v1.0.0`

### Rename previous commits

`git rebase -i HEAD~N`

### Rename previous merhe commit

`git checkout <HASH>`
`git commit --amend`
`git rebase HEAD <BRANCH_NAME>`

### Sources

[Git documentation](https://git-scm.com/)
[Cheat Sheets](https://www.xarg.org/cheat-sheet/git/)
