# Why learn how to use the command line?

The command line is an awesome tool with almost limitless functionality. Since you can directly control the computer by typing, many tasks can be performed more quickly, and some tasks can be automated with special commands that loop through and perform the same action on many files—saving you, potentially, loads of time in the process.

The application or user interface that accepts your typed responses and displays the data on the screen is called a shell, and there are many different varieties that you can choose from, but the most common these days is the Bash shell, which is the default on Linux and Mac systems in the Terminal application.

# What is the command line?

The command-line interface, sometimes referred to as the CLI, is a tool into which you can type text commands to perform specific tasks—in contrast to the mouse's pointing and clicking on menus and buttons.

Note: This article is meant for people who are either new to the command line or only have a couple of command-line tricks up their sleeve.

Open /Applications/Utilities/Terminal Keep in Dock for easy access.

In the terminal, first you see ```$```. This is called a shell prompt. It appears when the terminal is ready to accept a command.

When using the command line, we refer to folders as *directories*. Files and directories on your computer are organized into a *filesystem*. A filesystem organizes a computer's files and directories into a tree structure. The first directory in the filesystem is the *root directory*. It is the parent of all other directories and files in the filesystem.

Each directory can contain more files and child directories. The parent-child relationship continues as long as directories and files are nested.

# Navigating 

## Looking Around

```ls```: List all non-hidden files/folders

```ls -a```: List content including hidden files and directories. The ```-a``` is called an option. Options modify the behavior of commands. We use ```ls -a``` to display the contents of the working directory in more detail.

```ls -l```: Lists all contents of a directory in long format.

```ls -t```: Order files and directories by the time they were last modified.

```clear```: Clears the terminal window, moving the command prompt to the top of the screen.

*Note*: 
The options can be combined as ```ls -alt``` which lists all contents, including hidden files and directories, in long format, ordered by the date and time they were last modified.

## Moving Around

```pwd```: Print Working Directory: Displays the name of the directory you are currently in, called the *working directory*.

```cd```: Change Directory: Changes you into the directory you specify. In other words, cd changes the working directory. When a file, directory or program is passed into a command, it is called an argument. (case sensitive)

Note: Folders with spaces in name need to escape space: foo\ bar

```.```: Starts at current directory

```..```: Steps back a directory

```~``` : Represents the user's home directory.

## Files and Folders

```mkdir {folder-name}```:Make Directory: Makes It takes in a directory name as an argument, and then creates a new directory in the current working directory
.
Note: Folders with spaces in name need to escape space: foo\ bar

```touch {file-name}```: Will check to see if a file exists and, if it doesn't, a new file inside the working directory will be created. 

```rmdir {folder-name}```: Removes an empty directory

```cp <file_from> <file_to>```: The ```cp``` command copies files or directories.
--example:
```
cp frida.txt lincoln.txt
````

```cp *```: In addition to using filenames as arguments, we can use special characters like ```*``` to select groups of files. These special characters are called *wildcards*. The ```*``` selects all files in the working directory.

```mv```: Moves a file. Can rename while moving by changing file extension. To move a file into a directory, use ```mv``` with the source file as the first argument and the destination directory as the second argument. 

```rm```: Deletes file (does not move to trash, cannot undo)

```rm -r```: The -r stands for "recursive," and it's used to delete a directory and all of its child directories.

*Note*: Be careful when you use ```rm```! It deletes files and directories permanently. There isn't an undelete command, so once you delete a file or directory with ```rm```, it's gone.

```sort```: This takes the standard input and orders it alphabetically for the standard output.

OS X: ```open {file-or-folder}```
Linux: ```nautilus {file-or-folder}```
Windows: ```ii {file-or-folder} Opens a file or folder```
Opening ```.``` will open the current directory

## Redirection 
Through *redirection* you can direct the input and output of a command to and from other files and programs, and chain commands together in a pipeline. 

```echo "{content}" >```: Will write content to a file. The ```>``` command redirects the standard output to a file. 

--exmple: 
```
$ echo "Hello" > hello.txt
```
```
$ cat oceans.txt > continents.txt
```

```>>``` takes the standard output of the command on the left and appends (adds) it to the file on the right.

--example:
```
$ cat glaciers.txt >> rivers.txt
```

*Note*: ```>``` overwrites all original content in continents.txt.

```stdin```: Standard Input: Information inputted into the terminal through the keyboard or input device.
```stdout```: Standard Output: The information outputted after a process is run.
```stderr```: Standard Error: An error message outputted by a failed process.

```cat```: Will preview content in a file and outputs the contents of a file to the terminal. 

## Searching

```find {file-name}```: Finds files and folders. Use -type for specific types and -name for the name of files on non-Windows systems.

```grep "{search-term}"```: Global Regular Expression Print: It searches files for lines that match a pattern and returns the results. . Use ```-n``` for line numbers, ```-r``` to search recursively. Adding ```-i``` enables the command to be case insensitive.

```grep -R```: Searches all files in a directory and outputs filenames and lines containing matched results. ```-R``` stands for "recursive"

```grep -Rl```: Searches all files in a directory and outputs only filenames with matched results. ```-R``` stands for "recursive" and ```l``` stands for "files with matches"

```|```: Pipe. Generic way of passing the results from one command to another. You can think of this as "command to command" redirection.

## More 
```nano```: A command line text editor
```alias```: Allows you to create keyboard shortcuts, or aliases, for commonly used commands.
## That's all folks!

Feel free to bookmark this to refer back when hacking away on your own terminal. Leave a comment below for any suggestions or comments. Thank you
