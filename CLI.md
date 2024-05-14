# Command Line Instruction Equivalents

This markdown file provides a comparison of command line instructions between Linux/Unix and Windows.

# Table of Contents

- [File Operations](#file-operations)
- [Text Operations](#text-operations)
- [System Information](#system-information)
- [Package Management](#package-management)
- [User Management](#user-management)
- [Networking](#networking)
- [Miscellaneous](#miscellaneous)
- [Linux/Unix Commands in Depth](#linuxunix-commands-in-depth)
  - [`ls` - List Directory Contents](#ls---list-directory-contents)
  - [`grep` - Search Text](#grep---search-text)
  - [`find` - Search Files and Directories](#find---search-files-and-directories)
  - [`chmod` - Change File Permissions](#chmod---change-file-permissions)
  - [`tar` - Archive Files](#tar---archive-files)
  - [`awk` - Text Processing](#awk---text-processing)
- [Windows Commands in Depth](#windows-commands-in-depth)
  - [`dir` - List Directory Contents](#dir---list-directory-contents)
  - [`find` - Search Text in Files](#find---search-text-in-files)
  - [`ipconfig` - Network Configuration](#ipconfig---network-configuration)
  - [`tasklist` - List Running Processes](#tasklist---list-running-processes)
  - [`net` - Network Commands](#net---network-commands)
  - [`shutdown` - System Shutdown](#shutdown---system-shutdown)


## File Operations

| Task Description         | Linux/Unix Command     | Windows Command       |
|--------------------------|------------------------|-----------------------|
| List files in directory  | [`ls`](#ls---list-directory-contents)                   | [`dir`](#dir---list-directory-contents)                 |
| Change directory         | `cd directory_name`    | `cd directory_name`   |
| Create new directory     | `mkdir directory_name` | `mkdir directory_name`|
| Copy file                | `cp source_file destination_file` | `copy source_file destination_file` |
| Move/Rename file         | `mv source_file destination_file` | `move source_file destination_file` |
| Delete file/directory    | `rm file_name`         | `del file_name`       |
|                          |                        | `rmdir directory_name`|

## Text Operations

| Task Description         | Linux/Unix Command     | Windows Command       |
|--------------------------|------------------------|-----------------------|
| Display file content     | `cat file_name`        | `type file_name`      |
| Display first lines of file | `head file_name`     | `more file_name`      |
| Display last lines of file  | `tail file_name`     | `more file_name`      |
| Search for text in file  | [`grep 'pattern' file_name`](#grep---search-text) | `findstr 'pattern' file_name` |

## System Information

| Task Description         | Linux/Unix Command     | Windows Command       |
|--------------------------|------------------------|-----------------------|
| Display system info      | `uname -a`             | `systeminfo`          |
| Display IP address       | `ifconfig`             | [`ipconfig` ](#ipconfig---network-configuration)           |
| List running processes   | `ps aux`               | `tasklist`            |

## Package Management

| Task Description         | Linux/Unix Command     | Windows Command       |
|--------------------------|------------------------|-----------------------|
| Install package          | `apt-get install package_name` | `choco install package_name` |
| Update packages          | `apt-get update`       | `choco upgrade all`   |
| Remove package           | `apt-get remove package_name` | `choco uninstall package_name` |

## User Management

| Task Description         | Linux/Unix Command     | Windows Command       |
|--------------------------|------------------------|-----------------------|
| Add user                 | `adduser username`     | `net user username /add` |
| Change user password     | `passwd username`      | `net user username *` |
| Delete user              | `userdel username`     | `net user username /delete` |
|                          |                        | `net user username /delete` |

## Networking

| Task Description         | Linux/Unix Command     | Windows Command       |
|--------------------------|------------------------|-----------------------|
| Ping host                | `ping hostname`        | `ping hostname`       |
| Transfer files (SCP)     | `scp source_file user@hostname:destination_path` | `pscp source_file username@hostname:destination_path` |

## Miscellaneous

| Task Description         | Linux/Unix Command     | Windows Command       |
|--------------------------|------------------------|-----------------------|
| Display manual for command| `man command`          | `command /?`          |
| List environment variables| `printenv`             | `set`                 |
| Shutdown/restart system  | `shutdown`             | [`shutdown`](#shutdown---system-shutdown)            |

# Linux/Unix Commands in Depth

## `ls` - List Directory Contents

The `ls` command is used to list directory contents.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `ls -R`                      | List subdirectories recursively                      |
| `ls -l`                      | Use a long listing format (detailed information)    |
| `ls -a`                      | List all entries, including hidden files             |
| `ls -h`                      | Display file sizes in a human-readable format        |
| `ls -t`                      | Sort by modification time (newest first)             |
| `ls -r`                      | Reverse order while sorting                          |
| `ls -S`                      | Sort by file size (largest first)                    |
| `ls -i`                      | Display inode numbers                                |
| `ls --color`                 | Colorized output                                     |
| `ls --group-directories-first`| List directories first before files                  |
| `ls -v`                      | Sort by version numbers naturally within text         |
| `ls -d`                      | List directories themselves, not their contents       |
| `ls -1`                      | List one file per line                               |

## `grep` - Search Text

The `grep` command is used to search text.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `grep 'pattern' file`        | Search for a pattern in a file                      |
| `grep -i 'pattern' file`     | Case-insensitive search                             |
| `grep -r 'pattern' directory`| Recursively search for a pattern in a directory tree |
| `grep -n 'pattern' file`     | Display line numbers with matching lines             |

## `find` - Search Files and Directories

The `find` command is used to search for files and directories.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `find . -name 'filename'`    | Search for a file named 'filename' in the current directory and its subdirectories |
| `find . -type f`             | List all files in the current directory and its subdirectories |
| `find . -type d`             | List all directories in the current directory and its subdirectories |
| `find . -empty`              | List empty files and directories in the current directory and its subdirectories |

## `chmod` - Change File Permissions

The `chmod` command is used to change file permissions.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `chmod u+x file`             | Add execute permission for the owner                 |
| `chmod g-w file`             | Remove write permission for the group                 |
| `chmod o=r file`             | Set read-only permission for others                  |

## `tar` - Archive Files

The `tar` command is used to archive files.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `tar -cvf archive.tar file1 file2` | Create a new tar archive file                       |
| `tar -xvf archive.tar`       | Extract files from a tar archive                     |
| `tar -tvf archive.tar`       | List contents of a tar archive                       |

## `awk` - Text Processing

The `awk` command is used for text processing.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `awk '{print $1}' file`      | Print the first column of each line in a file        |
| `awk '/pattern/' file`       | Search for lines matching a pattern in a file         |
| `awk -F: '{print $NF}' file` | Print the last field of each line using ':' as a delimiter |

These are some commonly used Unix/Linux commands along with their options and extensions. Feel free to explore more options for each command by referring to their respective manual pages (`man <command>`).

# Windows Commands in Depth

## `dir` - List Directory Contents

The `dir` command is used to list directory contents in Windows.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `dir /S`                     | Display files in the specified directory and all subdirectories |
| `dir /A`                     | Display files with specified attributes              |
| `dir /B`                     | Bare format (file names only)                        |
| `dir /O`                     | Sort order (e.g., `/O:D` for sort by date)           |
| `dir /P`                     | Pause after each screen of information               |

## `find` - Search Text in Files

The `find` command is used to search for text in files in Windows.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `find "pattern" filename`    | Search for a pattern in a file                      |
| `find /C "pattern" filename` | Count occurrences of a pattern in a file             |
| `find /I "pattern" filename` | Case-insensitive search                              |

## `ipconfig` - Network Configuration

The `ipconfig` command is used to display and manage network configurations in Windows.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `ipconfig /all`              | Display detailed configuration information           |
| `ipconfig /release`          | Release the IP address assigned by DHCP              |
| `ipconfig /renew`            | Renew the IP address assigned by DHCP                |

## `tasklist` - List Running Processes

The `tasklist` command is used to list all running processes in Windows.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `tasklist /v`                | Display verbose task information                     |
| `tasklist /svc`              | Display services hosted by each process              |

## `net` - Network Commands

The `net` command is used for various network-related commands in Windows.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `net use`                    | Display or manage network connections                |
| `net user username *`        | Change user password                                 |
| `net start servicename`      | Start a specified service                            |

## `shutdown` - System Shutdown

The `shutdown` command is used to shut down or restart the system in Windows.

| Option/Extension             | Description                                         |
|------------------------------|-----------------------------------------------------|
| `shutdown /s`                | Shutdown the computer                                |
| `shutdown /r`                | Restart the computer                                 |
| `shutdown /t`                | Set the time delay before shutdown/restart           |

These are some commonly used Windows command line commands along with their options or extensions. Windows command line offers a range of functionalities similar to Unix/Linux commands, although the syntax and behavior might differ. Refer to the respective command's help (`command /?`) for more detailed information and additional options.
