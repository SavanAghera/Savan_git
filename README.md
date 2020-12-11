#Exercise 

#1
git clone git@github.com:SavanAghera/Savan_git.git
Savan_git/
mkdir new
nano new/1.txt
git add .
git commit -m "1 commit on master"
git push origin master

#2
git branch dev
git checkout dev 
mkdir dev
nano dev/1.txt
nano dev/2.txt
git add .
git commit -m "1 commit on dev"
git push origin master

#3
git branch branch1
git branch branch2
git checkout branch1
nano branch1.txt
git add .
git commit -m "1 commit on branch1"
git checkout branch2
nano branch2.txt
git add .
git commit -m "1 commit on branch2"

#4
git checkout branch1
nano branch1.txt
git add .
git commit -m "2 commit on branch1"

git checkout branch2
nano branch2.txt
git add .
git commit -m "2 commit on branch2"

#5
git chekout branch1
git commit --amend -m "2 commit on branch1 commit massage changed"
git chekout branch2
git commit --amend -m "2 commit on branch2 commit massage changed"

#6
git checkout branch1
git push origin branch1

git checkout branch2
git push origin branch2

#7
git checkout dev
git merge branch1 
git merge branch2

#8
##8a
git checkout branch1
nano branch1.txt
##8b
git stash save  "change in branch1"
git stash show
git checkout branch2
nano branch2.txt
git add .
##8c
git commit -m "3 commit on branch2 without ccommit branch1"
git  checkout branch1
git stash pop
git  add .
git commit -m "3 commit on branch1 after ccommit branch2"
git push origin branch1
git checkout branch2
git status
git push origin branch2

#9
##9a
git branch feature1
git branch feature2
##9b
git checkout feature1
nano feature1.txt
git add .
git commit -m "1 commit on feature1"
git checkout feture2
nano feature2.txt
git add .
git commit -m "1 commit on feature2"
##9c
git checkout feature1
git push origin feature1
##9d
git checkout feature2
git pull origin feature1
##9e
git checkout dev 
git merge feature1
##9f
git pull origin dev
##9g
git checkout feature2 
git push origin feature2
##9h
git rebase dev feature2 
git checkout dev
git merge feature2
git push origin dev

#end
