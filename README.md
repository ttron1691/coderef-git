# Code Reference for Git
## Installation
The Git CLI can be installed via
```Shell
# Linux
sudo apt-get install git
```
For Windows, the corresponding Git client can be downloaded form the official website [https://git-scm.com/](https://git-scm.com/). 
### Version
The git version can be checked via
```Shell
git --version
```
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
We can clone an exisiting Git repository via HTTPS or SSH (public/private key authentication) in the following way
```Shell
git clone [URL]

# Example
git clone https://github.com/ttron1691/coderef-git.git      # HTTPS
git clone git@github.com/ttron1691/coderef-git.git          # SSH
```
This will create a clone of the remove repository on the hard drive of the specified URL. Mostly this is used as a **local repository** in contrast to the **remote repository** which is typically hosted on a virtual machine and which is accessible via the web.
## Basic Commands
### Status
We can check for the status of the git repository by using
```Shell
git status    # Status regarding the staging area
```
### Difference
We can check for any changes in the files compared to the staging area by using
```Shell
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
## Commit
In Git a commit represents a current snapshot of the project's currently staged changes. A commit can be done via the following command (including a descriptive message for a given commit)
```Shell
git commit -m "Commit message"
```
## Fetch
### Checkout remote branch
In order to checkout a branch which exists on a remote repository only but currently not on the local repository we must fetch the remote branches first via
```Shell
git fetch --all
```
## Pull
## Push
## Branches
Git branches are used to separate a work package from the current main line (main/master branch). Basically a Git branch represents an independent line of development for the purpose of developing a new feature (feature branch) or fixing an existing bug (bug branch) or fixing an existing issue (hotfix branch). Eventually a branch can be merged to the main/master branch to incorporate the changes from the branch to the main line.
### Show branches
In order to show all Git branches within the Git repository we can use
```Shell
git branch
```
### Create new branch
A new branch can be created from the current commit (current HEAD) in the following way
```Shell
git branch [BRANCH-NAME]
```
### Checkout branch
We can checkout (switch working environment) a specific Git branch via
```Shell
git checkout [BRANCH-NAME]
``` 
We can create a new branch (based on current HEAD) and immediately checkout the new branch using the following command
```Shell
git checkout -b [BRANCH-NAME]
```
If we would like to create and checkout a new branch based on a different branch we can use
```Shell
git checkout -b [BRANCH-NAME-NEW] [BRANCH-NAME-EXISTING]
```
## Stash
Stashing is used in Git for those situations when you want to checkout a different branch, and you want to store changes that are currently not read to be committed. This can be done in Git via
```Shell
git stash [OPTIONS]
```
Further commands are given as follows
```Shell
git stash

git stash save "This is a message for the stash"

git stash list      # Showing information about the stashes
```
In order to re-apply the shashed changes we use
```Shell
git stash pop
```
## SSH Authorization

## Template
```Shell
TODO
```


## References
- Official Git website: [https://git-scm.com/](https://git-scm.com/)
- Github cheat sheet: [https://education.github.com/git-cheat-sheet-education.pdf](https://education.github.com/git-cheat-sheet-education.pdf)
