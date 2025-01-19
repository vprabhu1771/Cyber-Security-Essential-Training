# 1 - date

date command is used to display the system date and time. 

```bash
date
```

OUTPUT

```
Friday 20 January 2023 06:47:14 PM IST
```

# 2 - whoami

get the active username

```
whoami
```

OUTPUT

```
linux_rig2
```

# 3 - which
 
```bash
which python3

which nano
```

OUTPUT

```
/usr/bin/python3

/usr/bin/nano
```

# 4 - clear

Clear the terminal display

```bash
clear
```

# 5 - pwd

The `pwd` command allows you to print the current working directory on your terminal. It’s a very basic command and solves its purpose very well.

```bash
pwd
```

OUTPUT

```
/home/linux_rig2
```

# 6 - ls

The `ls` command is used to list files and directories in the current working directory. This is going to be one of the most frequently used Linux commands you must know of.

```bash
ls
```

OUTPUT

```
Desktop    Downloads  Music   Pictures  Videos
Documents  Public    Templates
```

# 7 - cd

While working within the terminal, moving around within directories is pretty much a necessity. The `cd` command is one of the important Linux commands you must know and it will help you to navigate through directories. Just type cd followed by directory as shown below.

```bash
cd <directory path>
```

# 8 - mkdir

Command used to create directories in Linux

```bash
mkdir folder_name
```

# 9 - rmdir

The `rm` command is used to delete files and folders and is one of the important Linux commands you must know.

```bash
rmdir <folder name>
```

To delete a directory, you have to add the `-r` argument to it. Without the `-r` argument, rm command won’t delete directories.

```bash
rmdir -r <folder name>
```

# 10 - cp

The `cp` and `mv` commands are equivalent to the copy-paste and cut-paste in Windows. But since Linux doesn’t really have a command for renaming files, we also make use of the mv command to rename files and folders.

```bash
cp <source> <destination>
```

# 11 - mv

In the Previous command, we created a copy of the file named Sample. Let’s see how what happens if we use the mv command in the same manner. For this demonstration, I’ll delete the Sample-Copy file.

```bash
mv <source> <destination
```

# 12 - exit

Exit Terminal 

```bash
exit
```

# 13 - cat

When you want to output the contents of a file, or print anything to the terminal output, we make use of the `cat` or `echo` commands.

```bash
cat <file name>
```

# 14 - uname

The `uname` and `whoami` commands allow you to know some basic information which comes really handy when you work on multiple systems. In general, if you’re working with a single computer, you won’t really need it as often as someone who is a network administrator.

```bash
uname
```

or

```bash
uname -a
```

# 15 - history

`history` command is used to view the previously executed command. This feature was not available in the Bourne shell. Bash and Korn support this feature in which every command executed is treated as the event and is associated with an event number using which they can be recalled and changed if required.

```bash
history 
```

OUTPUT

```
1  whoami
2  which python3
3  which nano
4  cat hell.sh
5  cat hello.sh
6  uname
7  help
```

To clear the history,

```bash
history -c
```

or

```bash
rm ~/.bash_history
```

# 16 - lsb_release

```bash
lsb_release -help
```

```bash
Usage: lsb_release [options]

Options:
  -h, --help         show this help message and exit
  -v, --version      show LSB modules this system supports
  -i, --id           show distributor ID
  -d, --description  show description of this distribution
  -r, --release      show release number of this distribution
  -c, --codename     show code name of this distribution
  -a, --all          show all of the above information
  -s, --short        show requested information in short format
```

```bash
lsb_release 

No LSB modules are available.
```

```bash
lsb_release -a
```

```
No LSB modules are available.
Distributor ID:	Debian
Description:	Debian GNU/Linux 11 (bullseye)
Release:	11
Codename:	bullseye
```