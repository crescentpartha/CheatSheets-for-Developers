Table of Contents
---

- [Git CheatSheet for Developers](#git-cheatsheet-for-developers)
  - [Git Configuration](#git-configuration)
  - [Getting & Creating Projects](#getting--creating-projects)
  - [Basic Commands](#basic-commands)
  - [Branching & Merging](#branching--merging)
  - [Sharing & Updating Projects](#sharing--updating-projects)
  - [Inspection & Comparison](#inspection--comparison)
  - [Tracking Path Changes](#tracking-path-changes)
  - [Setting up Alias](#setting-up-alias)
  - [Rewrite History](#rewrite-history)
  - [Deletion](#deletion)
  - [Temporary Commits](#Temporary-commits)

# Git CheatSheet for Developers

## Git Configuration

| Command | Description |
| ------- | ----------- |
| `git config` | Check all configuration options |
| `git config --list` | Check all configuration options with name and email |
| `git clone [https://url]` | Clone source code from a remote repository |

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
| `git diff` | Compare and show updated codes |
| `git add [file name]` | Add file changes in next commit |
| `git add .` | Add all unstaged changes in next commit |
| `git reset [file name]` | Used to unstage the staged files |
| `git clean -f` | To delete or remove unstaged files forcefully |
| `git commit -m "message about updates"` | Commit changes to current branch |
| `git commit -amend` | Amend with last commit but use the previous commit log message |
| `git rm [file]` | Deletes the file from your working directory and stages the deletion |
| `git pull` | Fetches and merges changes on the remote server to your working directory |
| `git fetch` | Gathers remote commits but does not merge them unlike `pull` |
| `git remote add origin [url]` | Adding a remote repository | 
| `git show` | Shows information about any git object |
| `gitk` | Shows graphical interface for a local repository |
| `git revert [commit-ID]` | Create new commit, reverting the changes from a specified commit |


**[🔼Back to Top](#table-of-contents)**

## Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches |
| `git branch [branch-name]` | Create a local branch |
| `git branch -d [branch-name]` | Delete a branch |
| `git branch -a` | See all branches (local and remote) |
| `git checkout [branch-name]` | Switch to another branch |
| `git switch [branch-name]` | Switch to another branch |
| `git merge [branch-name]` | Merge branchs |
| `git checkout -b "branch name"` | Create a new branch and switch to that branch |

**[🔼Back to Top](#table-of-contents)**

## Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git pull origin [branch name]` | Pull a branch from your remote repository |
| `git remote origin [branch name]` | Connect repository to local server |

**[🔼Back to Top](#table-of-contents)**

## Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --follow [file]` | Show the commits that changed file, even across renames |
| `git log --oneline` | View changes (briefly) |
| `git log branchB..branchA` | View changes on branchA that are not on branchB|
| `git log --graph` | Enables you to view your git log as a graph |
| `git log --decorate` | Makes git log display all of the references (e.g., branches, tags, etc) that point to each commit |
| `git log --author="name_of_author"` | Search for specific author |
| `git shortlog` | It groups each commit by author and displays the first line of each commit message |
| `git reflog ` | Git keeps track of updates to the tip of branches using a mechanism called reflog. This allows you to go back to changesets even though they are not referenced by any branch or tag |
| `git diff branchB...branchA` | View the differences of what is in branchA that are not on branchB |
| `git blame [file name]` | Display the modification on each line of a file |
| `git diff --name-only` | Show only names of changed files |


**[🔼Back to Top](#table-of-contents)**

## Tracking Path Changes

| Command | Description |
| ------- | ----------- |
| `git rm [file]` | Delete the file from project and stage the removal for commit |
| `git mv [existing-path] [new-path]`  | Change an existing file path and stage the move |
| `git log --stat -M`  | Show all commit logs with indication of any paths that moved |

**[🔼Back to Top](#table-of-contents)**
## Setting up Alias

| Command | Description |
| ------- | ----------- |
| `git config --global alias.[short name for command]  [actual command]` | Alias make the commands short and handy | (## ex:- git config --global alias.st status) |

**[🔼Back to Top](#table-of-contents)**

## Rewrite History
| Command | Description |
| ------- | ----------- |
|` git rebase [branch]`  | Apply any commits of current branch ahead of specified one |
| `git reset --hard [commit]`  | Clear staging area, rewrite working tree from specified commit |

**[🔼Back to Top](#table-of-contents)**

## Deletion
| Command | Description |
| ------- | ----------- |
| `git gc` | Cleans unnecessary files and optimizes the local repository |
| `git prune` | Deletes objects that don’t have any incoming pointers |

**[🔼Back to Top](#table-of-contents)**

## Temporary Commits
| command | Description |
| ------- | ----------- |
| `git stash`| Save modified and staged changes|
|`git stash list`| list stack-order of stashed file changes|
|`git stash pop`| write working from top of stash stack|
|`git stash drop` | discard the changes from top of stash stack|


**[🔼Back to Top](#table-of-contents)**
