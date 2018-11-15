# Git

## 2 Ways to have git (.git file) for your folder OR have git working

### First Way

#### Git clone in cmd

>git clone https://github.com/larwindcunha/wowremote.git

This will set up git and have upstream link and remote set.
Remote _origin_ means Github by default if cloned.
Main branch is called _master_.

### Second Way

#### Git init

* mkdir folder
* cd folder
* >git init
* >**git remote add remote_name repo_url** 
* "ADD files for pushing"
* >git status
* >git add .
* >git commit -m"Description, git add . will add all untracked files" or git commit -am"If git add . is not done
* >git push -u origin master

Pushing with -u for the first time is for setting upstream branch
After that from that branch git push is enough. It will know which branch to push to when in a particular branch(given upstream is set in that)

## Using GIT

* _git checkout branch-name_ will enter that branch branch-name
* _git checkout -b branch-name-new_ will create and enter the new branch branch-name

### If local branch _local-now_ is there and want to create branch of same name on remote then

_git push remote-origin localnow:localnow_
OR
_git push origin localnow:new-branch_

### Git push

_git push_ does git push origin master from that particular branch
_