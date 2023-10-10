# Lab Report 1
---
## *cd Command*
 *cd is a command used to change the current working directory.* <br>
 1. cd Command with no arguments: <br>
> Input:
> `user@sahara ~]$ cd` <br>
Nothing occurs as no arguments are passed to change the directory. <br>
While the output was not an error nothing occurred when using the command.
   ---
 2. cd Command with a Path to a Directory: <br>
> Input:
> `[user@sahara ~]$ cd lecture1` <br>
> Output:
> `[user@sahara ~/lecture1]$ `<br>
> Using the cd command the working directory changed as before using the cd command it was in the home directory, however now it is in /home/lecture1. <br>
> This can be seen using pwd:<br>
`[user@sahara ~/lecture1]$ pwd`<br>
`/home/lecture1`<br>
> In this case the output was not an error as the purpose of the cd command is to change the working directory, therefore it takes a directory path as an argument.<br>
   ---
 3. cd Command with a Path to a File: <br>
> Input:
> `[user@sahara ~/lecture1]$ cd Hello.class` <br>
> Output:
> `bash: cd: Hello.class: Not a directory `<br>
> Since cd changes a working directory, it needs to be given a path and not a file. <br>
> In this case the output was an error as Hello.class is a file and not a path so an error occurs.<br>
---


## *ls Command*
*The ls command is used to list out the files in the current directory* <br>
 1. ls Command with no arguments: <br>
> Input:
> `user@sahara ~]$ ls` <br>
> Output:
> `lecture1` <br>
> Since the ls command displays the list the files in the current directory, the files in the current directory is only `lecture1` <br>
The output was not an error 
   ---
 2. ls Command with a Path to a Directory: <br>
> Input:
> `[user@sahara ~]$ ls lecture1/messages` <br>
> Output:
> `en-us.txt  es-mx.txt  zh-cn.txt`<br>
> When passing a path as an argument with the ls command, it shows all the files in the that are in the path's directory.
> In this case the output was not an error <br>
   ---
 3. ls Command with a Path to a File: <br>
> Input:
> `[user@sahara ~]$ ls lecture1/Hello.class` <br>
> Output:
> `lecture1/Hello.class`<br>
> Since ls lists out the files in a given directory and not a file, although it isn't an output I expected, it outputted the path I used as an argument. This is because the file given as an argument is the only file in the directory, so therefore 'Hello.java' is given as an output.  <br>
> In this case the output was not an error.
---

## *cat Command*
*The cat command is used to print the contents of one or more files given by the path* <br>
1. cat Command with no arguments: <br>
 > Input:
 > `[user@sahara ~]$ cat` <br>
 > Output:
 > `   ` <br>
 > Since the cat command prints out the contents of a file, it needs arguments to do so. As a result of not having arguments, the terminal is stuck in a loop. <br>
 The output was an error as the terminal became stuck in a loop trying to print the contents of nothing.
   ---
 2. cat Command with a Path to a Directory: <br>
> Input:
> `[user@sahara ~]$ cat lecture1/messages` <br>
> Output:
> `cat: lecture1/messages: Is a directory`<br>
> Since we gave the cat command a path that led to a directory rather than a file, nothing could be printed and therefore an error showed. <br> 
> In this case the output was an error as the path did not lead to a file rather it just lead to a directory. <br>
   ---
 3. ls Command with a Path to a File: <br>
> Input:
> `[user@sahara ~]$ cat lecture1/messages/en-us.txt` <br>
> Output:
> `Hello World!`<br>
> "Hello World!" is the text inside of en-us.txt and the cat command printed out the contents of the file.  <br>
> In this case the output was not an error.
