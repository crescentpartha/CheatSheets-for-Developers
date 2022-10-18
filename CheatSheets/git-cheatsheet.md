Table of Contents
---

- [Git CheatSheet for Developers](#git-cheatsheet-for-developers)
  - [Git Configuration](#git-configuration)
  - [Getting & Creating Projects](#getting--creating-projects)
  - [Basic Commands](#basic-commands)
  - [Branching & Merging](#branching--merging)
  - [Sharing & Updating Projects](#sharing--updating-projects)
  - [Inspection & Comparison](#inspection--comparison)

# Git CheatSheet for Developers

## Git Configuration

| Command | Description |
| ------- | ----------- |
| `git config` | Check all configuration options |
| `git config -l` | List of information about your git configuration including user name and email |
| `git config --global user.email` | Setup the user email address you'll use in your commits. |
| `git config --global credential.helper cache` | You can store login credentials in the cache so you don't have to type them in each time. Just use this command: |


**[🔼Back to Top](#table-of-contents)**

## Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |

**[🔼Back to Top](#table-of-contents)**

## Basic Commands

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add filename_here` | The command below will add a file to the staging area |
| `git add .` | Add all files in your project to the staging area |
| `git add fil*` | With the asterisk in the command below, you can add all files starting with 'fil' in the staging area. |
| `git commit` | Captures a snapshot of the project's currently staged changes |
| `git commit -m "your commit message here"` | Commit changes with a message |  
| `git commit -a -m"your commit message here"` | Commit changes (and skip the staging area) |  
| `git mv oldfile newfile` | Rename files |
| `Create a .gitignore file and commit it.` | Ignore files |



**[🔼Back to Top](#table-of-contents)**

## Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch branch_name` | Create a new branch |
| `git branch` | List branches |
| `git checkout branch_name` | Switch to a newly created branch |
| `git checkout -b branch_name` | Create a branch in Git and switch to it immediately |
| `git branch -d branch_name` | Delete a branch |
| `git merge branch_name` | Merge two branches |
| `git merge origin/main` | Merge a remote repo with your local repo |


**[🔼Back to Top](#table-of-contents)**

## Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git add remote https://repo_here` | Add a remote repository |
| `git remote -v` | See remote URLs |
| `git remote show origin` | More info about a remote repo |
| `git push` | Push changes to a remote repo |
| `git pull` | Pull changes from a remote repo |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push --delete origin branch_name_here` | Remove a remote branch |
| `git rebase branch_name_here` | Transfer completed work from one branch to another |


**[🔼Back to Top](#table-of-contents)**

## Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log -p ` | See your commit history including changes |
| `git diff filename_here ` | See changes made before committing them using "diff" |
| `git add -p` |  See changes using "git add -p" |
| `git rm filename` | Remove tracked files from the current working tree |
| `git reset HEAD filename` | Revert staged changes |
| `git revert HEAD` | Rollback the last commit |
| `git revert comit_id_here` |  Rollback an old commit  |
| `git fetch` |  Fetch remote repo changes  |



**[🔼Back to Top](#table-of-contents)**

