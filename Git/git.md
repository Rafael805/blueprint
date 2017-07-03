## What is version control?

Version control systems are a category of software tools that help a software team manage changes to source code over time. Version control software keeps track of every modification to the code in a special kind of database. Developing software without using version control is risky, like not having backups. If a mistake is made, developers can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption to all team members.

For almost all software projects, the source code is like the crown jewels - a precious asset whose value must be protected. Version control protects source code from both catastrophe and the casual degradation of human error and unintended consequences. The code for a project, app or software component is typically organized in a folder structure or "file tree". One developer on the team may be working on a new feature while another developer fixes an unrelated bug by changing code, each developer may make their changes in several parts of the file tree.

## What is Git?

"Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency."

Git is a modern version control system. Git enables you to rewind to the part before you made a wrong turn and create a new destiny for your project. Basically, it is a way for developers to work with different versions of our code so we can safe different features, make notes as we progress, have different versions, and collaborate with different people. A staggering number of software projects rely on Git for version control, including commercial projects as well as open source.  If you have a big project Git is a very beneficial tool.

Git projects are usually managed on Github, a website that hosts Git projects for millions of users. With Github you can access your projects from anywhere in the world by using the basic workflow you learned here.

# Git Basics

The three usual commands you will use are:

```
1. git init
2. git add
3. git commit
```

## Create a new repository
First thing to do is create a new directory (runningmkdir on the command line). Open it and perform
```
git init
```

to initialize a new repository. This makes a hidden directory called .git which is where all of git exists.

## Check the status
Check the status of the files (to see what the current state of our project is)

```git status```

## Include a file to be tracked 
To tell Git to start tracking changes made to your file, we first need to add it to the staging area by using
```
git add
```

To at multiple files, you could add the changed files to the staging area with:
```
git add filename_1 filename_2
```

To add all files use:
```
git add *
```

## Commit the files 
To store the staged changes run the commit command with a message describing what has been changed.
```
git commit -m "Your message goes here"
```

Shortcut to commit and add if file is already being tracked
```
git commit -a -m "Your message goes here"
<combined>
git commit -am "Your message goes here"
```

# History
Use Git's log as a journal that remembers all the changes you've committed so far, in the order of files committed. Try running it now:
```
git log
```

To see the difference between a file as it appears in the working directory vs. how it appears in your last commit:
```
git diff
```

Use ```q``` to quit

# Backtrack
In Git, the commit you are currently on is known as the ```HEAD``` commit. In many cases, the most recently made commit is the ```HEAD``` commit.

To see the ```HEAD``` commit, enter:
```git show HEAD```

*Note:* The output of this command will display everything the git log command displays for the HEAD commit, plus all the file changes that were committed.

To restore the file in your working directory to look exactly as it did when you last made a commit use:
```git checkout HEAD <file_name>```

To unstage a file from the staging area use:
```git reset HEAD <file_name>```
This command resets the file in the staging area to be the same as the HEAD commit. It does not discard file changes from the working directory, it just removes them from the staging area.

*Note:* in the output, "Unstaged changes after reset":
```M    <file_name>```
```M``` is short for "modification"

To rewind to the part before you made the wrong turn and create a new destiny for the project:
```git reset SHA```

*Note:* This command works by using the first 7 characters of the SHA of a previous commit.

**Before reset:**

HEAD is at the most recent commit

**After reset:**
HEAD goes to a previously made commit of your choice. You have in essence rewinded the project's history

--example: If the SHA of the previous commit is 5d692065cf51a2f50ea8e7b19b5a7ae512f633ba
```git reset 5d69206```
To find the SHA ust ```git log```

#  Branching

Git allows us to create branches to experiment with versions of a project. In Git, branches are usually a means to an end. You create them to work on a new project feature, but the end goal is to merge that feature into the ```master``` branch. After the branch has been integrated into ```master```, it has served its purpose and can be deleted.

## Create branch
To create a new branch, use:

```git branch <branch_name>```

## Check branch
To check which branch you're on or to lists all a Git project's branches: 

```git branch```

The ```*``` (asterisk) will show you what branch you’re on

--example:

```* master```

## Switch branch
To switch from one branch to another:

```git checkout <branch_name>```

## Merge branch
To join file changes from one branch to another:

```git merge <branch_name>```

Git uses markings to indicate the HEAD (master) version of the file and the other version of the file, like this:

```
<<<<<<< HEAD
master version of line
=======
<other_version> version of line
>>>>>>> <other_version>
```

The merge is a "fast forward" because Git recognizes that the new branch contains the most recent commit. Git fast forwards master to be up to date with the new branch.

## Remove branch
To delete the specified branch from your Git project: 
```
git branch -d <branch_name>
```

## Remove files

To remove a file use:

```rm -rf```

# Remotes
In order to collaborate, you and your partner need:

+ A complete replica of the project on your own computers
+ A way to keep track of and review each other's work
+ Access to a definitive project version

You can accomplish all of this by using **remotes**. A remote is a Git repository that lives outside your Git project folder. Remotes can live on the web, on a shared network or even in a separate folder on your local computer. It is a shared Git repository that allows multiple collaborators to work on the same Git project from different locations. Collaborators work on the project independently, and merge changes together when they are ready to do so.

In order to get your own replica of a remote repository, you'll need to clone it with. The ```<remote_location>``` tells Git where to go to find the remote. This could be a web address, or a filepath (e.g ```/Users/teachers/Documents/some-remote```). The ```<clone_name>``` is the name you give to the directory in which Git will clone the repository.
```
git clone <remote_location> <clone_name>
```
Your clone is your local copy of the remote Git project. If you commit changes to your local copy, your partner will not know about them.  

One thing that Git does behind the scenes when you clone a remote is give the remote address the name *origin*, so that you can refer to it more conveniently. In this case, your partner's remote is origin.

You can see a list of a Git project's remotes with the command:
```
git remote -v
```
The remote is listed twice: once for ```(fetch)``` and once for ```(push)```  

An easy way to see if changes have been made to the remote and bring the changes down to your local copy is with:
```
git fetch
```
This command will not merge changes from the remote into your local repository. It brings those changes onto what's called a remote branch. 

Even though your partner's new commits have been fetched to your local copy of the Git project, those commits are on the ```origin/master``` branch. Your *local* ```master``` branch has not been updated yet, so you can't view or make changes to any of the work she has added.

Merge origin/master into your local master branch:
```
git merge origin/master
```

The workflow for Git collaborations typically follows this order:

1. Fetch and merge changes from the remote
2. Create a branch to work on a new project feature
3. Develop the feature on your branch and commit your work
4. Fetch and merge from the remote again (in case new commits were made while you were working)
5. Push your branch up to the remote for review

Steps 1 and 4 are a safeguard against merge conflicts, which occur when two branches contain file changes that cannot be merged with the ```git merge``` command. Step 5 involves ```git push```, a command you will learn in the next exercise.

To share our work with your partner and push your branch up to the remote, ```origin```. Your partner can then review your branch and merge your work into the ```master``` branch, making it part of the definitive project version.
```
git push origin <your_branch_name>
```
Git will inform you that your branch was pushed up to the remote. 
