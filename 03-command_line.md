# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](https://web.archive.org/web/20160708171659/http://cli.learncodethehardway.org/book/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. Each "chapter" focuses on a command. Type the commands you see in the _Do This_ section, and read the _You Learned This_ section. Move on to the next chapter. You should be able to go through these in a couple of hours.

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

* show current working directory path = pwd
* creating a directory = mkdir
* deleting a directory = rm -r
* creating a file using `touch` command = touch
* deleting a file = rm
* renaming a file = mv
* listing hidden files = ls -a
* copying a file from one directory to another = cp
* list all files in working directory = ls
* change working directory = cd
---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  Lists all files in the working directory (non hidden)
`ls -a`  List all files in the working directory including hidden
`ls -l`  Lists all files in the working directory in long format
`ls -lh`  Lists all files in the working directory in long format, with the file size abreviated e.g. K or M bytes
`ls -lah`  Lists all files including hidden in the working directory in long format, with the file size abreviated
`ls -t`  Lists all files in the working directory in order of the time they were last modified
`ls -Glp`  List all files in the working directory in long format, wihtout the group, and directories listed with an ending "/"

> > REPLACE THIS TEXT WITH YOUR RESPONSE

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

-a to show all files not just the non hidden ones
-h to show the abreviated file size
-l to show the full list of files
-m to list the files with commas
-p to differentiate the dirrectories and files

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

Xargs allows you to build and exicute command lines from a standard input
An example:
find -name "*.txt" | xarg grep "text"
would find any file that contained the listed text
 

