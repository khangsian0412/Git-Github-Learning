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
2. git reset HEAD~ : This helps you undo the last commit (the general form of reset actually rewrites history and undoes commit)
3. git restore: This brings you back to the last commit.
4. git revert: This creates a new commit that brings the project back tot he last commit. It leaves the whole timeline intact, it does not delete the old commit.  
4. git log: This allows you to view the commits that you've made

reset vs restore vs revert: Reset changes the pointer, which points to different commits on our timeline, and then it deletes every commit that comes after it. Restore is about fixing files, it would change it back to the last saved version. Revert is a milder version of reset. It creates a new commit instead bringing everything back in time, so the whole timeline is preserved. 


Branching 
1. main: It is formerly known as the master branch. 
2. Why branch: Instead of making changes at the main branch, we can create a new branch first and make our changes there. After we are ready then we merge it back to the main branch. 

Merge: It combines the changes from two branches into one.
1. (from dest) git merge <source> -m "message here": This merges the stuff fromt he source to the destination.  
2. Note that merging always creates a new commit, and can sometimes be messy 

Rebase 
1. git rebase <the source from which you want to rebase>: It is very aptly named, you change the base of your branch. Say someone made changes on your main branch after you branch off from it. You want to incorporate that, you can do so using rebase by changing the base to the new commit that the other person made on the main branch. 

Comparing commits: 
1. git diff <new commit> <old commit> : The order simply affects the perspective from which the differences are shown.

Push, Fetch and Pull 
1. git push: This uploads your local repository to Github 
2. git fetch: This fetches from Github to the local repo, but it does not merge with your working directory yet. 
3. git pull: This is basically fetch + merge.  

Stash (LIFO)
Git does not allow switching of branches when you have uncommitted changes. 
1. To switch branches with uncommitted work, you can use git stash
2. When you come back, you do git stash pop to restore the uncommitted chnages. 
3. If you don't want to pop if from the stash, use git stash apply instead. The things on the stash is still intact. 
4. git stash list shows you everything in the stash.
5. Since you can have multiple stashes, you can identify them with the unique ID, allowing you to access them individually. 
6. What to do after: You can remove a stash with git stash drop

Pull request 
The idea is that you cannot simply make changes to people's repo. If you want to merge your stuff to theirs, you have to make a pull request.  

Miscellaneous points: 
1. git rm filename.format: The idea is that you can simultaneously remove and file and stage that change in one command 
2. git rm --cahced: This only removes the file from staging, the actual file is NOT deleted. 
3. git rm --f: This removes the file from both the stage and from the local computer. 


