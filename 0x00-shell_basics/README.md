# Shell, basics
## Resources
- [What is the Shell](https://alx-intranet.hbtn.io/rltoken/vwO91sqNBgRL03BLu-ueiA)
- [Navigation](https://alx-intranet.hbtn.io/rltoken/iblidp7yp6i-QpT8rDXHaA)
- [Looking around](https://alx-intranet.hbtn.io/rltoken/xEKUCnQsMH0esQ6fJU5vLA)
- [A Guided Tour](https://alx-intranet.hbtn.io/rltoken/HUhQ73fFR1GOC5nb4r-mDw)
- [Manipulating Files](https://alx-intranet.hbtn.io/rltoken/olv-1tj4d1LA57Z0PrLNvw)
- [Working with Commands](https://alx-intranet.hbtn.io/rltoken/olv-1tj4d1LA57Z0PrLNvw)
- [Reading Man Pages](https://alx-intranet.hbtn.io/rltoken/rddGdsqLf8_kRzp12RaD4A)
- [Keyboard Shortcuts for Bash](https://alx-intranet.hbtn.io/rltoken/JcsRq7PW6v7SdpPH_N8udQ)
- [LTS](https://wiki.ubuntu.com/LTS)
- [Shebang](https://alx-intranet.hbtn.io/rltoken/cE8ZA3kgEaFhB-IDNv31bQ)
#### man or help:
- cd
- ls
- pwd
- less
- file
- ln
- cp
- mv
- rm
- mkdir
- type
- which
- help
- man
## Learning Objectives
### General

- What does RTFM mean?
- What is a Shebang

### What is the Shell

- What is the shell
- What is the difference between a terminal and a shell
- What is the shell prompt
- How to use the history (the basics)

### Navigation

- What do the commands or built-ins cd, pwd, ls do
- How to navigate the filesystem
- What are the . and .. directories
- What is the working directory, how to print it and how to change it
- What is the root directory
- What is the home directory, and how to go there
- What is the difference between the root directory and the home directory of the user root
- What are the characteristics of hidden files and how to list them
- What does the command cd - do

### Looking Around

- What do the commands ls, less, file do
- How do you use options and arguments with commands
- Understand the ls long format and how to display it
- A Guided Tour
- What does the ln command do
- What do you find in the most common/important directories
- What is a symbolic link
- What is a hard link
- What is the difference between a hard link and a symbolic link

### Manipulating Files

- What do the commands cp, mv, rm, mkdir do
- What are wildcards and how do they work
- How to use wildcards

### Working with Commands

- What do type, which, help, man commands do
- What are the different kinds of commands
- What is an alias
- When do you use the command help instead of man

### Reading Man Pages

- How to read a man page
- What are man page sections
- What are the section numbers for User commands, System calls and Library functions

### Keyboard Shortcuts for Bash

- Common shortcuts for Bash

### LTS

- What does LTS mean?

## Requirements
### General
- Allowed editors: vi, vim, emacs
- All your scripts will be tested on Ubuntu 20.04 LTS
- All your scripts should be exactly two lines long (```$ wc -l file``` should print 2)
- All your files should end with a new line ([why?](http://unix.stackexchange.com/questions/18743/whats-the-point-in-adding-a-new-line-to-the-end-of-a-file/18789))
- The first line of all your files should be exactly ```#!/bin/bash```
- A README.md file at the root of the repo, containing a description of the repository
- A README.md file, at the root of the folder of this project, describing what each script is doing
- You are not allowed to use backticks, &&, || or ;
- All your scripts must be executable. To make your file executable, use the chmod command: ```chmod u+x file```. Later, we’ll learn more about how to utilize this command.

#### Example
```
julien@ubuntu:/tmp$ ls
12-file_type
lll
julien@ubuntu:/tmp$ ls -la lll
-rw-rw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ cat lll
#!/bin/bash
ls
julien@ubuntu:/tmp$ ls -l lll
-rw-rw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ chmod u+x lll # you do not have to understand this yet
julien@ubuntu:/tmp$ ls -l lll
-rwxrw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ ./lll
12-file_type
lll
julien@ubuntu:/tmp$ 
```
## Tasks:
- 0-Write a script that prints the absolute path name of the current working directory.
- 1-Display the contents list of your current directory.
- 2-Write a script that changes the working directory to the user’s home directory.
- 3-Display current directory contents in a long format
- 4-Display current directory contents, including hidden files (starting with .). Use the long format.
- 5-Display current directory contents.
    Long format
    with user and group IDs displayed numerically
    And hidden files (starting with .)
- 6-Create a script that creates a directory named my_first_directory in the /tmp/ directory.
- 7-Move the file betty from /tmp/ to /tmp/my_first_directory.
- 8-Delete the file betty.
   - The file betty is in /tmp/my_first_directory
- 9-Delete the directory my_first_directory that is in the /tmp directory.
- 10-Write a script that changes the working directory to the previous one.
- 11-Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format.
- 12-Write a script that prints the type of the file named iamafile. The file iamafile will be in the /tmp directory when we will run your script.
- 13-Create a symbolic link to /bin/ls, named __ls__. The symbolic link should be created in the current working directory. 
- 14-Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.
- 15-Create a script that moves all files beginning with an uppercase letter to the directory /tmp/u.
- 16-Create a script that deletes all files in the current working directory that end with the character ~.
- 17-Create a script that creates the directories welcome/, welcome/to/ and welcome/to/school in the current directory.
- 18-Write a command that lists all the files and directories of the current directory, separated by commas (,).

    - Directory names should end with a slash (/)
    - Files and directories starting with a dot (.) should be listed
    - The listing should be alpha ordered, except for the directories . and .. which should be listed at the very beginning
    - Only digits and letters are used to sort; Digits should come first
    - You can assume that all the files we will test with will have at least one letter or one digit
    - The listing should end with a new line
- 19-Create a magic file school.mgc that can be used with the command file to detect School data files. School data files always contain the string SCHOOL at offset 0.
