<!-- Heading section doesn't work -->
<!-- ---
title: Linux CheatSheet
description: The most commonly used linux commands are given here.
created: 2022-10-21
--- -->

## Table of Contents

- [Linux CheatSheet for Developers](#linux-cheatsheet-for-developers)
  - [File Commands](#file-commands)
  - [File Permissions](#file-permissions)
  - [Privilege Escalation](#privilege-escalation)
  - [SSH](#ssh)
  - [System Info](#system-info)
  - [Shortcuts](#shortcuts)
  - [Text Editors](#text-editors)
  - [Archives](#archives)
  - [Disk Usage](#disk-usage)
  - [Search](#search)
  - [Networking](#networking)
  - [Environment Variables command](#environment-variables-command)

# Linux CheatSheet for Developers

## File Commands

| Command | Description |
| ------- | ----------- |
| `pwd` | Show current directory | 
| `mkdir dir` | Make directory called *dir* | 
| `mkdir -p folder/folder2` | Make a directory *folder* and another directory *folder2* in it|
| `cd dir` | Change directory to *dir* |
| `cd ..` | Go up a directory | 
| `cd` | Change to home directory |
| `ls` | List contents of directory|
| `ls -r` | Reverse list contents of directory |
| `ls -t` | List contents of directory based on time |
| `ls -al` | Formatted list of contents for the directory including hidden files |
| `rm file` | Delete file | 
| `rm -r dir` | Delete directory *dir* | 
| `rm -f file` | Forcibly delete the file | 
| `rm -rf dir` | Forcibly delete the directory *dir* | 
| `rm -rfv dir` | Forcibly delete the directory *dir* with verbose output |
| `cp file1 dir` | Copy *file1* to inside of *dir*| 
| `mv file1 dir` | Move/Cut *file1* to inside of *dir*| 
| `touch file` | Create *file*|
| `cat file` | Show the Contents of file | 
| `head file` | Display first 10 lines of files | 
| `tail file` | Display last 10 lines of files | 
| `gpg -c file` | Encrypt a file | 
| `gpg file` | Decrypt a file | 
| `wc` | Show the Number of words,lines,bytes in file |

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
| `free` | Display amount of free and used memory in the system |
| `w` | See who is online |
| `whoami` | See who you are logged in as|
| `uname -a` | Show kernel information |
| `man command` | Show the manual for any command (exit with **q**) 

**[🔼Back to Top](#table-of-contents)**

## Shortcuts

| Command | Description |
| ------- | ----------- |
| `Ctrl + A` | Moves the cursor to the start of a line |
| `Ctrl + E` | Moves the cursor to the end of the line |
| `Ctrl + F` | Move one character forward |
| `Ctrl + B` | Move one character backward |
| `Ctrl + L` | Clear the terminal screen |
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

## Archives
| Command | Description |
| ------- | ----------- |
| `tar cf archive.tar directory` | Create tar named archive.tar containing directory |
| `tar xf archive.tar` | Extract the contents from archive.tar |
| `tar czf archive.tar.gz directory` | Create a gzip compressed tar file name archive.tar.gz|
| `tar xzf archive.tar.gz` | Extract a gzip compressed tar file|
| `tar cjf archive.tar.bz2 directory` | Create a tar file with bzip2 compression|
| `tar xjf archive.tar.bz2` | Extract a bzip2 compressed tar file|

**[🔼Back to Top](#table-of-contents)**

## Disk Usage
| Command | Description |
| ------- | ----------- |
| `df -h` | Show free and used space on mounted filesystems |
| `df -i` | Show free and used inodes on mounted filesystems |
| `fdisk -l` | Display disks partitions sizes and types|
| `du -ah` | Display disk usage for all files and directories in human readable format|
| `du -sh` | Display total disk usage off the current directory|

**[🔼Back to Top](#table-of-contents)**

## Search
| Command | Description |
| ------- | ----------- |
| `grep pattern file` | Search for pattern in file |
| `grep -r pattern directory` | Search recursively for pattern in directory |
| `locate name` | Find files and directories by name|
| `find /home/xyz -name 'prefix*'` | Find files in /home/xyz that start with "prefix" |
| `find /home -size +100M` | Find files larger than 100MB in /home|

**[🔼Back to Top](#table-of-contents)**

## Networking
| Command | Description |
| ------- | ----------- |
| `ip a` | Display all network interfaces and IP address |
| `ip addr show dev eth0` | Display eth0 address and details |
| `ethtool eth0` | Query or control network driver and hardware settings|
| `ping host` | Send ICMP echo request to host |
| `whois domain` | Display whois information for domain|
| `dig domain` | Display DNS information for domain|
| `dig -x IP_ADDRESS` | Reverse lookup of IP_ADDRESS|
| `host domain` | Display DNS IP address for domain|
| `hostname -i` | Display the network address of the host name|
| `hostname -I` | Display all local IP addresses of the host|
| `wget http://domain.com/file` |Download http[]()://domain.com/file |
| `netstat -nutlp` |Display listening tcp and udp ports and corresponding programs|

**[🔼Back to Top](#table-of-contents)**

## Environment variables command
| Command | Description |
| ------- | ----------- |
| `env` | Displays all environment variables |
| `echo $VARIABLE` | Displays value of variable |

**[🔼Back to Top](#table-of-contents)**
