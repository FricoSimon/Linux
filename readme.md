# Linux Ubuntu Commands

This README contains a list of Linux Ubuntu commands.

## Glossary

- `su`: Super User
- `sudo`: the highest tier of command
- `apt`: Advanced Package Tool
- `dpkg`: Debian Package Manager
- `stdin`, `stdout`, `stderr`: standard input / output / error
- `grep`: Global Regular Expression Print
- `ps`: Process Status

## Commands

### Update repository and system:

```bash
sudo apt update
```

### Upgrade repository and system:

```bash
sudo apt upgrade
```

### Print value inside a document:

```bash
cat [ -n ] FILENAME
```

### Print the beginning value of a document:

```bash
head [ -NUMBER OF LINE ] FILENAME
```

### Print the end value of a document:

```bash
tail [ -NUMBER OF LINE ] FILENAME
```

### Show current directory (path):

```bash
pwd
```

### Change directory:

```bash
cd DIRECTORY PATH
```

- Move up one directory level

```bash
cd ..
```

- Back to previous directory

```bash
cd -
```

- Go to user's home directory

```bash
cd ~s
```

- Go to root directory

```bash
cd /
```

### Show directory as a tree:

```bash
tree [ -d ] [ -a ]
```

### Show list:

```bash
ls [ -all ] [ -long ] [ *keyword filename* ]
```

### Show directory only:

```bash
dir
```

### Create file:

```bash
touch [ -timestamp ] FILENAME
```

### Rename file:

```bash
mv old FILENAME new FILENAME
```

### Remove file:

```bash
rm [ -f ] [ -i ] FILENAME
```

### Create link (hard & soft):

- Hardlink (strict as edit in one file affect others)

```bash
ln PATH_TO_FILE1 PATH_TO_FILE2
```

- Softlink (more flexible)

```bash
ln -s PATH_TO_FILE1 PATH_TO_FILE2
```

### Add directory to list (stack):

```bash
pushd DIRECTORY PATH
```

### Back to original directory (stack):

```bash
popd
```

### Create and delete directory:

- Create

```bash
mkdir DIRECTORY NAME
```

- delete

```bash
rmdir DIRECTORY NAME
```

### Remove directory and its content forcefully:

```bash
rm -rf DIRECTORY NAME
```

### Output direction:

```bash
> FILENAME
```

(example: `echo "hello world" > hello.txt`)

### Pipeline (combine several commands into one):

```bash
|
```

### Search file and directory:

```bash
locate KEYWORD
```

### Search and manipulate text:

- Print all except the keyword

```bash
grep [ -v ]
```

- Count the number of keyword appears

```bash
grep [ -c ]
```

- Print the lines

```bash
grep [ -n ]
```

- Ignore case sensitive

```bash
grep [ -i ]

```

- Search not only in its directories but also in all of its subdirectories

```bash
grep [ -r ]
```

### Manipulate text (stream editor):

```bash
sed 's/OLD TEXT/NEW TEXT/' FILENAME
```

(use `-i` to change the file)

### Text processing:

```bash
awk
```

(example: `ps | awk '{print $1}'`, `awk -F ":" '{print $1}' /etc/passwd` - use `-F` for field separator)

### Documentation (manual pages):

```bash
man COMMAND
```

- More extensive

```bash
info COMMAND
```

### Show all processes in this terminal:

- Show parent process

```bash
ps [ -f ]
```

- Show all processes

```bash
ps [ -ef ]
```

### Display disk space:

- Human readable format

```bash
df [ -h ]
```

### Redirect output file:

`>`: overwrites file and creates if it doesn't exist <br>
`>>`: appends file and creates if it doesn't exist

### Nano text editor:

```bash
nano FILENAME
```

### Vim text editor:

```bash
sudo apt install vim
```

```bash
vim FILENAME
```

- Tutorial

```bash
vimtutor
```

### Create new user:

```bash
sudo adduser USERNAME
```

### Delete a user:

```bash
sudo userdel USERNAME
```

- Delete user's folder

```bash
sudo rm -rf /home/USERNAME
```

### Change password for a user:

- User

```bash
passwd
```

- Admin

```bash
sudo passwd USERNAME
```

- List all users in Linux:

```bash
ls -l /home
```

(usually they have their own folder)

```bash
cat /etc/passwd
```

- Export environment variable:

```bash
export VARIABLE_NAME=VARIABLE_VALUE
```

- List history of commands used:

```bash
history
```

- Change ownership of a file:

```bash
chown NEW_USER FILENAME
```

- Change permissions of a file:

```bash
chmod XXX FILENAME
```

(1 = execute permission, 2 = write permission, 4 = read permission; first x = owner, second x = group, third x = everyone)

- Create a shell script file:

```bash
NAME.sh
```

(add `#! /bin/sh`)

- Find command:

```bash
find PATH -name FILENAME
```

(use `-t` for type F / D, `-exec` to execute command for all items)

- System monitoring (CPU, memory, etc.):

```bash
top
```

```bash
htop
```

```bash
free
```
