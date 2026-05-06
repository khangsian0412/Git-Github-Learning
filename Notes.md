<Notes> 

The whole Git workflow goes as such: 
Working directory --> Stage (a transitional period) --> Repository (commit). 

How to start a new Git project? 
1. Locally: You can do it by using normal terminal commands, like mkdir for directories, and touch for new files. Use git init to initialise. 
2. Remotely: You can create a new repository on Github along with new files within it. Git is automatically initialised for you when you create the repository. 

Staging: 
1. git add -A & git add --all: These two commands adds ALL the changes made to the whole project. 
2. git add .: This dot version adds only the changes that you make in the CURRENT directory and everything within.
3. git add * : This star version adds changes OTHER THAN DELETED files. Basically if you delete something, that change will not be added if you use that command. 
4. git add <file name>: This version allows you to add specific files. 

How to reset: get reset. This undoes whatever you have added and brings it back to the previous version. 
