# Linux Ubuntu Commands

This README contains a list of Linux Ubuntu commands.

## Glossary

- `su`: Super User
- `apt`: Advanced Package Tool
- `dpkg`: Debian Package Manager
- `stdin`, `stdout`, `stderr`: standard input / output / error
- `grep`: Global Regular Expression Print
- `ps`: Process Status

## Commands

- `sudo`: the highest tier of command
- Update repository and system: `sudo apt update`
- Upgrade repository and system: `sudo apt upgrade`
- Print value inside a document: `cat [ -n ] FILENAME`
- Print the beginning value of a document: `head [ -NUMBER OF LINE ] FILENAME`
- Print the end value of a document: `tail [ -NUMBER OF LINE ] FILENAME`
- Show current directory (path): `pwd`
- Change directory:
  - `cd`
  - `cd ..` (move up one directory level)
  - `cd -` (back to previous directory)
  - `cd ~` (go to user's home directory)
  - `cd /` (go to root directory)
- Show directory as a tree: `tree [ -d ] [ -a ]`
- Show list: `ls [ -all ] [ -long ] [ *keyword filename* ]`
- Show directory only: `dir`
- Create file: `touch [ -timestamp ] FILENAME`
- Rename file: `mv old FILENAME new FILENAME`
- Remove file: `rm [ -f ] [ -i ] FILENAME`
- Create link (hard & soft):
  - `ln PATH_TO_FILE1 PATH_TO_FILE2` (hardlink) - strict as edit in one file affect others
  - `ln -s PATH_TO_FILE1 PATH_TO_FILE2` (softlink) - more flexible
- Add directory to list (stack): `pushd DIRECTORY PATH`
- Back to original directory (stack): `popd`
- Create and delete directory:
  - `mkdir DIRECTORY NAME`
  - `rmdir DIRECTORY NAME`
- Remove directory and its content forcefully: `rm -rf DIRECTORY NAME`
- Output direction: `> FILENAME` (example: `echo "hello world" > hello.txt`)
- Pipeline (combine several commands into one): `|`
- Search file and directory: `locate KEYWORD`
- Search and manipulate text: `grep [ -v ]` (print all except the keyword), `grep [ -c ]` (count the number of keyword appears), `grep [ -n ]` (print the lines), `grep [ -i ]` (ignore case sensitive), `grep [ -r ]` (search not only in its directories but also in all of its subdirectories)
- Manipulate text (stream editor): `sed 's/OLD TEXT/NEW TEXT/' FILENAME` (use `-i` to change the file)
- Text processing: `awk` (example: `ps | awk '{print $1}'`, `awk -F ":" '{print $1}' /etc/passwd` - use `-F` for field separator)
- Documentation (manual pages): `man COMMAND`, `info COMMAND` (more extensive)
- Show all processes in this terminal: `ps [ -f ]` (show parent process), `ps [ -ef ]` (show all processes)
- Display disk space: `df [ -h ]` (human readable format)
- Redirect output file:
  - `>`: overwrites file and creates if it doesn't exist
  - `>>`: appends file and creates if it doesn't exist
- Nano text editor: `nano FILENAME`
- Vim text editor: `sudo apt install vim`, `vim FILENAME`, `vimtutor` (tutorial)
- Create new user: `sudo adduser USERNAME`
- Delete a user: `sudo userdel USERNAME`, `sudo rm -rf /home/USERNAME` (delete user's folder)
- Change password for a user: `passwd` (user), `sudo passwd USERNAME` (admin)
- List all users in Linux: `ls -l /home` (usually they have their own folder), `cat /etc/passwd`
- Export environment variable: `export VARIABLE_NAME=VARIABLE_VALUE`
- List history of commands used: `history`
- Change ownership of a file: `chown NEW_USER FILENAME`
- Change permissions of a file: `chmod XXX FILENAME` (1 = execute permission, 2 = write permission, 4 = read permission; first x = owner, second x = group, third x = everyone)
- Create a shell script file: `NAME.sh` (add `#! /bin/sh`)
- Find command: `find PATH -name FILENAME` (use `-t` for type F / D, `-exec` to execute command for all items)
- System monitoring (CPU, memory, etc.): `top`, `htop`, `free` (memory only)
