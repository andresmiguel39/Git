# Git repository starting


### Create Staring


```bash

echo "My Project Desc" >> README.md

git init

git add README.md

git commit -m "first commit"

git remote add origin git@github.com:username/new_repo

git remote add origin https://github.com/username/new_repo

git push -u origin <BrachWhereIWantToCommitOrMaster> #Origin does know where to push changes

```


### Tipical git comands

```bash


 git status (git status)

 git add . (git add)

 git commit -m "[26]…" (git commit)

 git status 

 git log --online (show all changes)

 git log --oneline (show all changes one line)

 git checkout master

 git pull --rebase origin master

 git checkout rama

 git rebase master (actualizarse a master)

```


### For amends in commit

```bash


 Git commit —amend

 Git push -f origin <branch>

 git -D <>  # delete branch 

 Git branch # branch existentes

 Git checkout # selectionar rama 

 Git --amends # para escribir los cambios 

```