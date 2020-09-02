# Some notes about linux command line tools

These notes aim to be a TL;DR version of [this](https://tldp.org/LDP/GNU-Linux-Tools-Summary/html/index.html) guide <br/>
This is by no means an exhaustive list. It is intended to cover basic usage (I arbitrarily defined "basic usage" as until chapter 7) <br/>
The guide itself goes into much more detail than what I do here. If you find yourself itching for more, please do consult it

## Actual notes

### General shell commands

* `alias` lists current aliases, `unalias` removes aliases. An alias is a substitution of a command by another. Some useful examples:

  ```
  In your ~/.bashrc file

  alias cp='cp -vi' # prompt when copying if you want to overwrite and will tell you where information is going 
  alias rm='rm -i' # prompts you if you really want to remove it
  alias mv='mv -i' # prompts you if you are going to overwrite something
  ```
  *Note: Using a backslash (`\`) before a command overrides its alias*

* `history` shows you the history of commands you typed. `history n` will show you the last *n* commands you typed
  * `!n` will run the last *n* command
  * `!cd` will run the last command starting with `cd`

### Help commands

* `man <command>` will search for a manual page for the typed command. `info` also provides information on a program

* `whatis <command>` provides a one-liner description of the `command` argument

### Redirecting input/output

* `>` symbol sends information somewhere <br/>
  * `cat file1 file2 > file1_and_2.txt` will concatenate the files together into one big file named *file1_and_2.txt*. Note that this will overwrite any existing file

* As an opposite to `>`, `<` will use information as input to another program <br/>
  * `tr '[A-Z]' '[a-z]' < fileName.txt` would insert the contents of “fileName.txt” into the input of `tr`

* "pipe" (`|`) allows output of one program to be used as input to another <br/>
  * `cat filename.txt | grep hello` would print lines from "filename.txt" that contain "hello"

* `tee` sends the output of a program to a file and to standard output. Think of it as a T intersection...it goes two ways <br/>
  * `ls /home/user | tee my_directories.txt` would list the files on the standard output and print them to "my_directories.txt"

### Running multiple commands

* `command1 && command2` executes `command2` if `command1` performs successfully, like a logical **and**

* `command1 || command2` executes `command2` if `command1` fails, like a logical **or**

* `command1; command2` executes `command2` regardless of `command1` result

* `command1 & command2` executes both `command1` and `command2` in parallel

### Working with the file system

* Use `cd` to change to a different directory. Possible arguments include:
  * `..`, representing the parent directory
  * An aboslute path, like `/etc/paths`, representing exctly the mentioned path
  * A relative path, like `personal-stuff/texts`, representing `/.../<the_path_you_were_on_before/personal-stuff/texts>`

* `ls` will list files and directories. Refer to the `man` page for its full usage. Some popular options:
  * `-l` will list in long format including permissions, size, modification date and ownership
  * `-a` stands for "show all" and will list hidden files and directories. By default `ls` will not list entries that start with *.*

* `pwd` means "print working directory". It will print the current absolute path.

* `tree` recursively lists files and directories below the current one in a pretty tree format

### Working with files and folders

* `mkdir` creates a new directory in the current path

* `rm` removes files and directories, depending on options. Refer to the `man` page for further information

* Use `mv` to move files and directories. The same tool can be used to rename files and directories

* `cp` copies files and directories.  Refer to the `man` page for options and arguments

* `touch` is used to create an empty new file. It can also be used to change any file´s timestamp
