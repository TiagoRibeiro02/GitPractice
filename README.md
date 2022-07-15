# GitPractice
 Repository for git/github practice

## Summary of what I learned:
git init

git add .

git status

git commit -m "title" -m "description"

git log or git log --oneline

## To see how a certain state was and to get back to the last one
* git checkout ID
* git checkout master

## Makes a new commit that reverts everything that was made in that commit ID
git revert ID // work as an UNDO
-> Change header and CTRL+X+YES 

## Take us back in time to ID but the next ID's still there but they are not commited
git reset ID

## Take us back in time to ID but doesnt retain any changes from the commits after that one
git reset ID --hard

git push -f origin master // To update the GitHub repository with old stuff (only works with -f)

## Create a new branch called __BRANCHNAME__
git branch __BRANCHNAME__

## Show us the current branches
git branch -a 

## Take us to the __BRANCHNAME__
git checkout __BRANCHNAME__

## To delete __BRANCHNAME__ (we need to travel to branch master first)
* git checkout master
* git branch -D BRANCHNAME

## Create a new branch called __BRANCHNAME__ and checkout her (travels to her)
git checkout -b 'BRANCHNAME'

## To merge branches
* git checkout master
* git merge BRANCHNAME

## If there is any conflit when merging
1. Open the file(s) where the conflits happend
2. Delete what was done in HEAD(master) branch 
3. git commit (doesnt need a message)

Done...
---
## To push (from me to the respository)
* git init // If we havent any repository cloned
*Add files*
* git status // To see if there is anything to commit
* git add .
* gir commit -m "..."
* git push URL master // To push to the online repository what is in branch master
* git remote add origin URL // Add the alias "origin" to the URL, so we can do something like:
git push origin master // master is the name os the branch 
---
## To clone 
* git clone URL
* cd REPOSITORYNAME
**Make the changes**
* git remote -v // to see the alias
* git push origin master
---
## To colaborate
* git clone URL
* git checkout master
* git pull origin master // To update the files (from repository to me)
* git checkout -b __BRANCHNAME__ // Always work on a new branch
*ADD STUFF*
* git add .
* git commit -m "msg"
* git push origin __BRANCHNAME__
---
## In GitHub:
 - Compare & Pull request
 - Add some message etc...
 - Create pull request // it means that we want to merge the branches
 - The "repository boss" will look the changes and decide if merging the branches is a good idea
 - After that he can delete your branch, if he wants to
