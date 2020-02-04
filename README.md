# git-lab

# ** Status ** 

This project was generated with to give solutions to all users that need IT solution in Jabil.

[![Website shields.io](https://img.shields.io/website-up-down-green-red/http/shields.io.svg)](http://shields.io/)
[![Generic badge](https://img.shields.io/badge/version-1.0.0-green.svg)](https://shields.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)

----------

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

### Sources

[Git documentation](https://git-scm.com/)

