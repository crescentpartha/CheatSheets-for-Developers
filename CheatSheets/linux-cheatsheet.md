## Table of Contents
---

- [Linux CheatSheet for Developers](#linux-cheatsheet-for-developers)
  - [File Commands](#file-commands)
  - [File Permissions](#file-permissions)
  - [Privilege Escalation](#privilege-escalation)
  - [SSH](#ssh)
  - [System Info](#system-info)
  - [Shortcuts](#shortcuts)
  - [Text Editors](#text-editors)

# Linux CheatSheet for Developers

## File Commands

| Command | Description |
| ------- | ----------- |
| `pwd` | Show current directory | 
| `mkdir dir` | Make directory called *dir* | 
| `cd dir` | Change directory to *dir* |
| `cd ..` | Go up a directory | 
| `cd` | Change to home directory |
| `ls` | List contents of directory|
| `ls -al` | Formatted list of contents for the directory including hidden files |
| `rm file` | Delete file | 
| `rm -r dir` | Delete directory *dir* | 
| `rm -f file` |Force delete file | 
| `rm -rf dir` | Force delete directory *dir* | 
| `cp file1 dir` | Copy *file1* to inside of *dir*| 
| `mv file1 dir` | Move/Cut *file1* to inside of *dir*| 
| `touch file` | Create *file*| 


**[🔼Back to Top](#table-of-contents)**

## File Permissions

| Command | Description |
| ------- | ----------- |
| `chmod octal file` | Change the permissions of file to octal for user, group and world by adding: **4 - read( r ), 2 - write( w ), 1- execute ( x )**|
| `chmod 777 file` | Read, write, execute for all| 
| `chmod 755 file` | rwx for owner, rx for group and world.| 

**[🔼Back to Top](#table-of-contents)**

 ## Privilege Escalation
 
| Command | Description |
| ------- | ----------- |
| `sudo command` | Runs *command* as root. (If a command requires a higher permission you might have to run it with sudo)|
| `su` | Runs an interactive shell as root |

**[🔼Back to Top](#table-of-contents)**

## SSH

| Command | Description |
| ------- | ----------- |
| `ssh user@host` | Connect to host as user |
| `ssh -p port user@host` | Connect to host on port *port* as user|


**[🔼Back to Top](#table-of-contents)**

## System Info

| Command | Description |
| ------- | ----------- |
| `date` | Show the system date and time |
| `cal` | Show this month's calendar |
| `uptime` | Show system's uptime |
| `w` | See who is online |
| `whoami` | See who you are logged in as|
| `uname -a` | Show kernel information |
| `man command` | Show the manual for any command (exit with **q**) 

**[🔼Back to Top](#table-of-contents)**

## Shortcuts

| Command | Description |
| ------- | ----------- |
| `Ctrl + C` | Halts the current command |
| `Ctrl + D` | Log out of current session |
| `Ctrl + W` | Erases one word in current line |
| `Ctrl + U` | Erases entire line |

**[🔼Back to Top](#table-of-contents)**

## Text Editors
| Command | Description |
| ------- | ----------- |
| `nano file` | nano  is  a  small and friendly editor |
| `vi file` | vi is a powerful text editor where every action is done though the keyboard. [How to exit vim/vi](https://www.cyberciti.biz/faq/linux-unix-exit-vim-editor/) (Trust me you'll need to know it) |
| `vim file` | vim - Vi IMproved is an improved version of the vi editor. Like vi, every action is done through the keyboard.|

**[🔼Back to Top](#table-of-contents)**
