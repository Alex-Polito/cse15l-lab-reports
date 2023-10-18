```
[user@sahara ~]$ cd
[user@sahara ~]$
```
The working directory is /home. This command is meant to change the directory
to the specified path. Since the specified path is empty, it stays in the /home 
directory. When tested from a different working directory, the new directory is
/home.
This is not an error.
```
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$
```
The working directory is /home. The output is the main directory Lecture1 
because it is the only directory in the parent directory /home. 
This is not an error.
```
[user@sahara ~]$ cat

```
The working directory is /home. The output is empty because I did not provide
paths to concatenate. This is not an error.
```
[user@sahara ~]$ cd /home/lecture1
[user@sahara ~lecture1]$
```
The working directory was /home when the command was run. The output was a change
in directory, which can be seen in the next line after the tilde. From here out
(unless changed again) the working directory will stay as lecture1. This 
is not an error.
```
[user@sahara ~lecture1]$ ls /home/lecture1
Hello.class Hello.java messages README
[user@sahara ~lecture1]$
```
The working directory was lecture1. The output is all the contents directly
accessible in lecture1. This is a display command so did not change anything,
just displays the contents of lecture1. This is not an error.
```
[user@sahara ~lecture1]$ cat /home/lecture1/messages
cat: /home/lecture1/messages: Is a directory
[user@sahara ~lecture1]$
```
The working directory was lecture1. The output is a message that the file I'm 
attempting to display is a directory, because cat is meant to display file contents.
This is an error message because directories do not have file contents, but instead 
have files inside them. It would not make sense for cat to display contents of a 
folder because that is the role of ls.
```
[user@sahara ~lecture1]$ cd Hello.java
bash: cd: Hello.java: Not a directory
[user@sahara ~lecture1]$
```
The working directory was lecture1. Since Hello.java is a file and not a directory,
it does not make sense to set the directory to Hello.java. This is an error warning
that the file I'm trying to assign as the directory is not a directory.
```
[user@sahara ~lecture1]$ ls Hello.java
Hello.java
[user@sahara ~lecture1]$
```
The working directory was lecture1. Hello.java does not contain any files/folders, 
so the output is just the file Hello.java. This is not an error message.
```
[user@sahara ~lecture1]$ cat messages/en-us.txt
Hello World!
[user@sahara ~lecture1]$
```
The working directory was lecture1. cat is meant to display the contents of a 
file, and it does exactly that. since en-us.txt is a file with contents, and not
a directory, cat can print the contents. This is not an error message.
