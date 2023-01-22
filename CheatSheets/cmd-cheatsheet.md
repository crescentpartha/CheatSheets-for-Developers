---
title: CMD CheatSheet
description: The most commonly used cmd commands are given here.
created: 2022-10-25
---

## Table of Contents

- [CMD CheatSheet for Developers](#cmd-cheatsheet-for-developers)
- [RAA (Run As Administrator)](#raa-run-as-administrator)
  - [File and Folder Management:](#file-and-folder-management)
  - [Applications and Processes:](#applications-and-processes)
  - [Disk Management:](#disk-management)
  - [System Information:](#system-information)
  - [Network:](#network)
  - [Command Line Setup:](#command-line-setup)

# CMD CheatSheet for Developers

# RAA (Run As Administrator)

## File and Folder Management:

|       Command       | Description                                                                                   |
| :-----------------: | --------------------------------------------------------------------------------------------- |
|         `?`         | Help or sometimes shows related commands to some commands.                                    |
|        `ls`         | Showing all the existing folders in current directory                                         |
|        `cd`         | - To change directory <br /> - `cd directory-name`.                                           |
|       `copy`        | Copies files to another location                                                              |
|        `dir`        | List directory content.                                                                       |
|        `del`        | Used to delete one or more files.                                                             |
|      `expand`       | Decompresses compressed files.                                                                |
|        `fc`         | File compare- fc a.txt b.txt.                                                                 |
|       `find`        | Find files.                                                                                   |
|       `ftype`       | Display file type and mapping.                                                                |
|       `mkdir`       | Make a directory.                                                                             |
|       `move`        | Moves files from one folder to another.                                                       |
|       `print`       | Prints out the text file contents.                                                            |
|        `rm`         | - File remove from any directory <br /> - `rm file-name`.                                     |
| `rd` <br /> `rmdir` | - Removes the directory <br /> - `rmdir [dir]` <br /> - `rd [dir]`                            |
|     `rmdir /s`      | - Remove all the Subfolder from any Main-Folder <br /> - `rmdir /s folder-name`.              |
|      `dir /a`       | This command is help to find all the hidden directories                                       |
|        `ren`        | Rename.                                                                                       |
|      `replace`      | Replaces files in one directory with files of the same name in another directory.             |
|     `robocopy`      | Uses an advanced tool to copy files and directories.                                          |
|       `tree`        | Show all system folder in tree manner.                                                        |
|       `type`        | Displays the contents of text files.                                                          |
|       `xcopy`       | The xcopy command can copy one or more files or directory trees from one location to another. |

**[🔼Back to Top](#table-of-contents)**

## Applications and Processes:

|  Command   | Description                                                                                                                                  |
| :--------: | -------------------------------------------------------------------------------------------------------------------------------------------- |
| `schtasks` | Executes a command or start a scheduled application (Task Scheduler).                                                                        |
| `shutdown` | - Shutdown your computer, control system shutdown using additional commands <br /> - `shutdown` <br /> - `shutdown/?` <br /> - `shutdown/i`  |
| `tasklist` | Display a list of currently-running tasks                                                                                                    |
| `taskkill` | - Kills the running task <br /> - `taskkill /im [programme-name]` <br /> - `taskkill /im notepad.exe` <br /> - `taskkill /f /im notepad.exe` |
|   `reg`    | Starts registry editor                                                                                                                       |
|  `runas`   | Launches the task as another user                                                                                                            |

**[🔼Back to Top](#table-of-contents)**

## Disk Management: 

|           Command           | Description                                                                                        |
| :-------------------------: | -------------------------------------------------------------------------------------------------- |
|          `chkdsk`           | - Scan the disk/drive errors <br /> - `chkdsk [disk-name]:` <br /> - `chkdsk C:`                   |
|          `defrag`           | Starts disk defragmentation.                                                                       |
|          `compact`          | Displays and change the compression of files in NTFS partitions.                                   |
|          `format`           | Formats the disk.                                                                                  |
|          `Recover`          | Recovers data from a bad or damaged disk.                                                          |
|            `sfc`            | - System file checker, scans all system files and repairs them if required <br /> - `sfc /scannow` |
|            `vol`            | Displays volume label and serial number for the disk.                                              |
| `wmic logicaldisk get name` | Get all the drive name                                                                             |
|       `diskmgmt.msc`        | Open disk-management system from command prompt                                                    |

**[🔼Back to Top](#table-of-contents)**

## System Information:  

|   Command    | Description                                                                          |
| :----------: | ------------------------------------------------------------------------------------ |
|    `date`    | Show/Set date.                                                                       |
|  `hostname`  | Shows hostname of the computer.                                                      |
|  `powercfg`  | - Gives report of the power setting <br /> - `powercfg /?` <br /> - `powercfg /list` |
| `systeminfo` | To get system-related information.                                                   |
|    `time`    | Displays or sets the system time.                                                    |
|    `ver`     | Display operating system version.                                                    |
|   `finger`   | Information about the user.                                                          |
|   `whois`    | This command is useful when users want to find the domain name or the IP address.    |
|    `ftp`     | Transfer file to a ftp server.                                                       |
|   `getmac`   | Display mac address.                                                                 |
|    `mode`    | Used to configure system devices.                                                    |
|   `print`    | Print a specified text file to a specified printing device.                          |

**[🔼Back to Top](#table-of-contents)**

## Network: 

|   Command    | Description                                                                                                                                                                                                                                                     |
| :----------: | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|  `ipconfig`  | Display IP network settings.                                                                                                                                                                                                                                    |
|    `ping`    | - Test the ability of the source computer to reach a specified destination computer <br /> - Show the list of ___usage___ and ___options___ in cmd <br /> - Get a response from the website network <br /> - `ping [website name]` <br /> - `ping [ip address]` |
|  `nslookup`  | Finds IP address by resource name.                                                                                                                                                                                                                              |
|   `route`    | This command is used to check and make changes to the route table of the computer.                                                                                                                                                                              |
|    `arp`     | Shows a table with IP addresses converted into physical addresses.                                                                                                                                                                                              |
|   `netsh`    | - Allows you to display or modify the network configuration of a computer that is currently running <br /> - Commands used for various properties related to network <br /> - `netsh` _(step-1)_ <br /> - `netsh> /?`                                           |
| `netsh wlan` | - Command extension to the netsh <br /> - `netsh` _(step-1)_ <br /> - `netsh> wlan /?`                                                                                                                                                                          |

**[🔼Back to Top](#table-of-contents)**

## Command Line Setup: 
 
|    Command    | Description                                                                    |
| :-----------: | ------------------------------------------------------------------------------ |
|     `cls`     | Clear screen.                                                                  |
|    `color`    | Changes text and background color.                                             |
|    `echo`     | Print the after echo text once.                                                |
|   `prompt`    | Changes the command line prompt (print the after text until you close the cmd) |
|    `pause`    | Pause your window until you press any key.                                     |
|    `title`    | Title your command prompt.                                                     |
| `timeout xxx` | Countdown wait in terminal- xxx in seconds.                                    |
|    `exit`     | Exit from the cmd window.                                                      |
|    `reset`    | The reset command executed as reset session.                                   |

**[🔼Back to Top](#table-of-contents)**

