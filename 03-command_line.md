# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

`pwd`--**show current working directory**  
`mkdir`--**creating a directory**  
`rmdir`--**deleting a directory**  
`touch file_nam.extension`--**creating a file using `touch` command**  
`rm my_file.extension`--**deleting a file**  
`mv my_old_file.extension my_new_file.extension`--**renaming a file**  
`ls -a `--**listing hidden files**  
`cp my_file.extension new_directory/my_file.extension`--**copying a file from one directory to another**  
`cd path/to/go/to`--**change directory**
`locate \*my\* \*file\*`--**finds a specific file in the OS with the words 'my' and 'file'**  

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls` 
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > `ls`--lists all contents of working directory  
`ls -a`--lists all contents of working directory(including hidden files)  
`ls -l`--lists all contents of working directory one line at a time  
`ls -lh`--lists all contents of working directory with human readable format  
`ls-lah`--lists all contents of working directory(including hidden files) in human readable format  
`ls -t`--lists all contents of working directory sorted by modification time, newest first  
`ls -Glp`--lists all contents of working directory one line at a time (without owner) in '/' indicator appended to directories  


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > `ls -R`--recursively list all contents in subdirectories
`ls -LS`--sorts file by file size
`ls -d`--lists only directories
`ls -u`--lists files by access time
`ls -r`--lists files in reverse order

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > builds and executes command lines from standard input (helps to execute repeated commands)  
ex:  
`xargs find -name "\*.txt"`--this will find all files (including subdirectories) with extension '.txt'
 

