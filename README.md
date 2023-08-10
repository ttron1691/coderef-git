# Code Reference for Git
## Basic Commands
We can check for the status of the git repository by using
```Shell
git status    # Status regarding the staging area
git diff      # Status  
```
## Staging area
If we want to stage files to the staging area we add those files via
```Shell
git add [FILENAME]

# Examples
git add README.md
git add src/
```
Removing files from the staging area works as follows
```Shell
git add [FILENAME]

# Examples
git reset info.txt
git reset template.html 
```
## Remote Repository
In order to show the URL of the remote repository we may use the following command
```Shell
git remote -v
# origin git@github.com/ttron1691/coderef-git.git (fetch)
# origin git@github.com/ttron1691/coderef-git.git (push)
```
This typically shows the URL depending on the protocol of use
```Shell
# HTTPS
https://github.com/ttron1691/coderef-git.git
# SSH
git@github.com/ttron1691/coderef-git.git
```
