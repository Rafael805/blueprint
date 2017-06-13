## What is version control?

Version control systems are a category of software tools that help a software team manage changes to source code over time. Version control software keeps track of every modification to the code in a special kind of database. Developing software without using version control is risky, like not having backups. If a mistake is made, developers can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption to all team members.

For almost all software projects, the source code is like the crown jewels - a precious asset whose value must be protected. Version control protects source code from both catastrophe and the casual degradation of human error and unintended consequences. The code for a project, app or software component is typically organized in a folder structure or "file tree". One developer on the team may be working on a new feature while another developer fixes an unrelated bug by changing code, each developer may make their changes in several parts of the file tree.

## What is Git?

"Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency."

Git is a modern version control system. Basically, it is a way for developers to work with different versions of our code so we can safe different features, make notes as we progress, have different versions, and collaborate with different people. A staggering number of software projects rely on Git for version control, including commercial projects as well as open source.  If you have a big project Git is a very beneficial tool.

## Git Basics

The three usual commands you will use are:

```
1. git init
2. git add
3. git commit
```

### Create a new repository

First thing to do is create a new directory (runningmkdir on the command line). Open it and perform

```
git init
```

to initialize a new repository. This makes a hidden directory called .git which is where all of git exists.

### Check the status

Check the status of the files (to see what the current state of our project is)

```
git status
```

### Include a file to be tracked 

To tell Git to start tracking changes made to your file, we first need to add it to the staging area by using

```
git add
```

### Commit the files 

To store the staged changes run the commit command with a message describing what has been changed.

```
commit -m "Your message goes here"
```

### History

Use Git's log as a journal that remembers all the changes you've committed so far, in the order of files committed. Try running it now:

```
git log
```

Use ```q``` to quit

### Remove files

To remove a file use:

```
rm -rf
```
