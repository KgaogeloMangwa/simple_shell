ALX Simple Shell Team Project

This is an ALX collaboartaion project on Shell. Our shell can be called hsh
The project was completed using C language, shell and Betty linter

Description
hsh is a simple UNIX command language interpreter that reads commands from either a file or standard input and excutes them.

<<<<<<< HEAD
hsh prints a prompt and wait for a command from the user
hsh creates a child process in which the command is checked
The child process is replaced by the command that accepts arguments after which the program returns to the parent process and prints the prompt. Then the program is ready to receive a new command. 
hsh checks for built-ins, aliases in the pathh and local executable programs
hsh works in non-interactive modes also.
=======
More Info
Output
Unless specified otherwise, your program must have the exact same output as sh (/bin/sh) as well as the exact same error output.
The only difference is when you print an error, the name of the program must be equivalent to your argv[0] (See below)
Example of error with sh:

$ echo "qwerty" | /bin/sh
/bin/sh: 1: qwerty: not found
$ echo "qwerty" | /bin/../bin/sh
/bin/../bin/sh: 1: qwerty: not found
$
Same error with your program hsh:

$ echo "qwerty" | ./hsh
./hsh: 1: qwerty: not found
$ echo "qwerty" | ./././hsh
./././hsh: 1: qwerty: not found
$

# List of allowed functions and system calls
access (man 2 access)
chdir (man 2 chdir)
close (man 2 close)
closedir (man 3 closedir)
execve (man 2 execve)
exit (man 3 exit)
_exit (man 2 _exit)
fflush (man 3 fflush)
fork (man 2 fork)
free (man 3 free)
getcwd (man 3 getcwd)
getline (man 3 getline)
getpid (man 2 getpid)
isatty (man 3 isatty)
kill (man 2 kill)
malloc (man 3 malloc)
open (man 2 open)
opendir (man 3 opendir)
perror (man 3 perror)
read (man 2 read)
readdir (man 3 readdir)
signal (man 2 signal)
stat (__xstat) (man 2 stat)
lstat (__lxstat) (man 2 lstat)
fstat (__fxstat) (man 2 fstat)
strtok (man 3 strtok)
wait (man 2 wait)
waitpid (man 2 waitpid)
wait3 (man 2 wait3)
wait4 (man 2 wait4)
write (man 2 write)

# Compilation
## Your shell will be compiled this way:

`gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh`


# files
- README.md - description about the project repo
- man_1_simple_shell - is the man page for the shell we are going to write.
- AUTHORS - file at the  root of your repository, listing all individuals having contributed content to the repository.
- main.h - is the header file which contains the standared header file and prototype of o function used in the program.
- main.c - initialize the program with infinite loop by call the prompt function
- prompt.c - it use get-line system call to read the input from the user and run infinite loop with fork to keep prompt going.
- special_character - It identifies if the special inputs such as if the frist input is slash,the user typed exit or env...
- string.c -it handles the strings(string length, write string,find string in directory,concatane strings....)
- cmd.c - it finds the command the user entered.
- execute.c - execute the command.

## How to add Author file
`Bash script for generating the list of authors in git repo`
```
#!/bin/sh

git shortlog -se \
  | perl -spe 's/^\s+\d+\s+//' \
  | sed -e '/^CommitSyncScript.*$/d' \
  > AUTHORS
  ```
>>>>>>> c4fa23d6c1edd250bbd78908d120b54fb917f45e
