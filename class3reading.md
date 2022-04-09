[<=== Back](readme.md)

# Git / GitHub and ACP
Summarized from:
[Git Tutorial](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#1)

## What is Version Control?
A Version Control is a system that allows the user to share code with others, for multiple developers to work on code simultaneously, review changes to code, and revert a file to a previous version.

## What is Git?
Git is a Distributed Version Control system (DVCS) which is made of of file "snapshots". It mostly uses local resources, not relying on a server or internet connection. Every chang that is made to a file is tracked by Git.

### Importing
To import an existing project or directory:
- Switch to target project's directory ***cd***
- Use ***git init*** command
- To start tracking these files
> ___git add *.c___   
> ***git add LICENSE***   
>  ***git commit -m "add a message"***

### Cloning
Create a copy of a Git repository
>***git clone(URL)***

To clone into a different directory, add the name after the URL

### Workflow
The local Git repository has three components:
>**Working Directory** ===> **Index** ===> **Head**
- The Working Directory is where the actual files are located
- The Index is used for staging changes
- The Head points to the most recent commit

## ACP
ACP refers to the process of ADDING, COMMITING, and PUSHING changes from your local drive to the live project.

- Clone file from GitHub with ***git clone (URL)***
- Open VSC with ***code .***
- **ADD** changes to your file in VSC, then Ctrl+S to Save
- In the Terminal,  ***git add (name of file that was changed)*** 
- Check status with ***git status***
- **COMMIT** changes and leave a message ***git commit -m "leave a PUBLIC informational message here"***
- To **PUSH** changes to live site, use ***git push origin main***