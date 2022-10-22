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
| `git commit -m "message about updates"` | Commit changes to current branch |
| `git rm [file]` | Deletes the file from your working directory and stages the deletion |
| `git pull` | Fetches and merges changes on the remote server to your working directory |
| `git fetch` | Gathers remote commits but does not merge them unlike `pull` |
| `git remote add origin [url]` | Adding a remote repository | 
| `git show commit-id` | Replace commit-id with the id of the commit that you find in the commit log after the word commit.|
| `git log -p` | Shows the commit's history including all files and their changes |


**[🔼Back to Top](#table-of-contents)**

## Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches |
| `git branch [branch-name]` | Create a local branch |
| `git branch -d [branch-name]` | Delete a branch |
| `git checkout [branch-name]` | Switch to another branch |
| `git merge [branch-name]` | Merge branchs |
| `git checkout -b "branch name"` | Create a new branch and switch to that branch |

**[🔼Back to Top](#table-of-contents)**

## Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git pull origin [branch name]` | Pull a branch from your remote repository |
| `git remote origin [branch name]` | Connect repository to local server |
| `git rebase -i main` | Clean up a branches commits before rebasing onto main |

**[🔼Back to Top](#table-of-contents)**

## Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |

**[🔼Back to Top](#table-of-contents)**

