## Table of Contents

# CMD CheatSheet for Developers

## Some common and useful CMD commands 
# RAA(Run As Administrator)

# File and Folder Management:

| Command                  | Description                                                              |
| ------------------------ | -------------------------------------------------------------------------|
| `?`                      | help or sometimes shows related commands to some commands.               |
| `cd`                     | to open directory- cd<space>directory name.                              |
| `copy`                   | Copies files to another location                                         |
| `dir`                    | list directory content.                                                  |
| `del`                    | used to delete one or more files.                                        |
| `expand`                 | Decompresses compressed files.                                           |
| `fc`                     | file compare- fc a.txt b.txt.                                            |
| `find`                   | find files.                                                              |
| `ftype`                  | display file type and mapping.                                           |
| `mkdir`                  | make a directory.                                                        | 
| `move`                   | Moves files from one folder to another.                                  |
| `print`                  | Prints out the text file contents.                                       |
| `rd or rmdir`            | Deletes a folder.                                                        |
| `ren`                    | rename.                                                                  |
| `replace`       | Replaces files in one directory with files of the same name in another directory. |
| `robocopy`               | Uses an advanced tool to copy files and directories.                     |
| `tree`                   | show all system folder in tree manner.                                   |
| `type`                   | Displays the contents of text files.                                     |
| `xcopy`                  | The xcopy command can copy one or more files or directory trees from one location to another. |


# Applications and Processes:

| Command                  | Description                                                              |
| ------------------------ | -------------------------------------------------------------------------|
| `schtasks`               | Executes a command or start a scheduled application (Task Scheduler).    |
| `shutdown`-shutdown/?, try - shutdown/i | shutdown your computer, control system shutdown using additional commands. |
| `tasklist`               | shows the current running tasks in the system.                           |
| `taskkill`               | kills the running task, taskkill /im <programname>                       |
| `reg`                    | starts registry editor.                                                  |
| `runas`                  | Launches the task as another user.                                       |


# Disk Management: 

| Command                  | Description                                                              |
| ------------------------ | -------------------------------------------------------------------------|
| `chkdsk` try- chkdsk C:  | check the disk, chkdsk<space><diskname>:                                 |
| `defrag`                 | Starts disk defragmentation.                                             |
| `compact`                | Displays and change the compression of files in NTFS partitions.         |
| `format`                 | Formats the disk.                                                        |
| `Recover`                | Recovers data from a bad or damaged disk.                                |
| `sfc` - RAA              | System file checker.                                                     |
| `vol`                    |  Displays volume label and serial number for the disk.                   |


# System Informantion: 

| Command                  | Description                                                              |
| ------------------------ | -------------------------------------------------------------------------|
| `date`                   | show/set date.                                                           |
| `hostname`               | shows hostname of the computer.                                          |
| `powercfg`s- powercfg /? | gives report of the pwoer setting.                                       |
| `systeminfo`             | to get system-related information.                                       |
| `time`                   | Displays or sets the system time.                                        |
| `ver`                    | display operating system version.                                        |
| `finger`                 | information about the user.                                              |
| `whois`                  | This command is useful when users want to find the domain name or the IP address. |
| `ftp`                    | transfer file to a ftp server.                                           |
| `getmac`                 | dispaly mac address.                                                     |
| `mode`                   | used to configure system devices.                                        |
| `print`                  | print a specified text file to a specified printing device.              |


# Network: 

| `ipconfing`              | display IP network settings.                                             |
| `ping`                   | get a response from the website network, ping<website name>              |
| `nslookup`               | Finds IP address by resource name.                                       |
| `route`                  | This command is used to check and make changes to the route table of the computer. |
| `arp`                    | Shows a table with IP addresses converted into physical addresses.       |
| `netsh`                  | commands used for various properties related to network, try- netsh/?    |
| `netsh wlan`             | command extension to the netsh, try netsh wlan /?                        |


# Command Line Setup: 
  
| `cls`                    | clear screen.                                                            |
| `color`                  | changes text and background color.                                       |
| `echo`                   | print the after echo text once.                                          |
| `prompt`                 | Changes the command line prompt.(print the after text until you close the cmd.) |
| `pause`                  | pause your window until you press any key.                               |
| `title`                  | title your command prompt.                                               |
| `timeout xxx`            | countdown wait in terminal- xxx in seconds.                              |
| `exit`                   | exit from the cmd window.                                                |
| `reset`                  | the reset command executed as reset session.                             |
