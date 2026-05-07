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

How to reset: get reset. This undoes whatever you have added and brings it back to the previous version. Note that it doesn't actually undo the changes, it just unstages them. 

To also undo the actual changes made: git reset --hard  

Commit: 
Note that committing on your local machine simply saves a version of that code, it is not reflected on Github just yet. 
1. git commit -m "whatever message you want to include with the commit"
2. git reset HEAD~ : This helps you undo the last commit 
3. git log: This allows you to view the commits that you've made


Branching 
1. main: It is formerly known as the master branch. 
2. Why branch: Instead of making changes at the main branch, we can create a new branch first and make our changes there. After we are ready then we merge it back to the main branch. 

Merge: It combines the changes from two branches into one.
1. (from dest) git merge <source> -m "message here": This merges the stuff fromt he source to the destination.   


Miscellaneous points: 
1. git rm filename.format: The idea is that you can simultaneously remove and file and stage that change in one command 
2. git rm --cahced: This only removes the file from staging, the actual file is NOT deleted. 
3. git rm --f: This removes the file from both the stage and from the local computer. 


