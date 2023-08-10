# Code Reference for Git
## Setup
Set username and e-mail address of git user
```Shell
git config --global user.name "[firstname lastname]"
git config --global user.email "[valid-email]"
```
### Color settings
Set corresponding color scheme for git
```Shell
git config --global color.ui auto
```
## Initialize Git Repository
We can initialize an exisiting directory as a new git repository in the following way
```Shell
git init
```
Initialize a bare git repository
```Shell
git init --bare [DIRECTORY]
```
## Clone an existing Git Repository
We can clone an exisiting Git repository via HTTPS or SSH in the following way
```Shell
git clone [URL]

# Example
git clone https://github.com/ttron1691/coderef-git.git
git clone git@github.com/ttron1691/coderef-git.git
```
## Basic Commands
We can check for the status of the git repository by using
```Shell
git status    # Status regarding the staging area
git diff      # Status with respect to unstaged lines
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
## References
We refer to the Github cheat sheet which can be found under: https://education.github.com/git-cheat-sheet-education.pdf
