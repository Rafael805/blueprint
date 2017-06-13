# Why learn how to use the command line?

The command line is an awesome tool with almost limitless functionality. Since you can directly control the computer by typing, many tasks can be performed more quickly, and some tasks can be automated with special commands that loop through and perform the same action on many files—saving you, potentially, loads of time in the process.

The application or user interface that accepts your typed responses and displays the data on the screen is called a shell, and there are many different varieties that you can choose from, but the most common these days is the Bash shell, which is the default on Linux and Mac systems in the Terminal application.

# What is the command line?

The command-line interface, sometimes referred to as the CLI, is a tool into which you can type text commands to perform specific tasks—in contrast to the mouse's pointing and clicking on menus and buttons.

Note: This article is meant for people who are either new to the command line or only have a couple of command-line tricks up their sleeve.

Open /Applications/Utilities/Terminal Keep in Dock for easy access.

## Looking Around

ls: List all non-hidden files/folders

ls -a: List all files/folders

ls -l: Details list of available files/folder. Note: Can be combined with -a

## Moving Around

pwd: Displays your current path.

cd: Changes directory to entered directory (case sensitive)

Note: Folders with spaces in name need to escape space: foo\ bar

.: Starts at current directory

. .: Steps back a directory

~ : Starts at your user directory

## Files and Folders

mkdir {folder-name}: Makes a folder.
Note: Folders with spaces in name need to escape space: foo\ bar

rmdir {folder-name}: Removes an empty directory

touch {file-name}(Windows: New-Item {file-name} -type file: Will check to see if a file exists and, if it doesn't, create it

echo "{content}" >: Will write content to a file
cat: Will preview content in a file

mv: Moves a file. Can rename while moving by changing file extension

rm: Deletes file (does not move to trash, cannot undo)

rm -r: Deletes a not-empty directory (does not move to trash, cannot undo)

OS X: open {file-or-folder}
Linux: nautilus {file-or-folder}
Windows: ii {file-or-folder} Opens a file or folder.
Opening . will open the current directory

## Searching

find {file-name} (Windows: Get-ChildItem {file-name}): Finds files and folders. Use -type for specific types and -name for the name of files on non-Windows systems.

grep "{search-term}" (Windows: select-string .\*.* -pattern "{search-term}": Find content inside of files. Use -n for line numbers, -r to search recursively

|: Pipe. Generic way of passing the results from one command to another

## That's all folks!

Feel free to bookmark this to refer back when hacking away on your own terminal. Leave a comment below for any suggestions or comments. Thank you
