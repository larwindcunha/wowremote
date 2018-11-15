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

* _git branch branch-name_ will create a branch of the current working branch and will have all it's files
* _git checkout -b branch-name-new_ will create and enter the new branch branch-name
* _git checkout branch-name_ will enter that branch branch-name

### Git push

**_git push_ does git push origin master for that particular branch only** and this is done so that we do not need to _git push origin branch-name_ while in same branch with upstream.
But when in different branch and want to push, need to use full command _git push origin branch-name_ and this will only push (while in other branch) if commits are made in branchname branch.

### If local branch local-now is there and want to push and create branch of diff name on remote then

* _git push remote-origin localnow:new-branch_

### If local branch local-branch is there and want to push to remote but branch is not there then

* _git push origin localnow_

This will create remote branch of the same name as that of local branch.
Then _git push -u origin local-now_ will set upstream to it and _git push would be enough.

### Pushing

If any commits are done in any branch, for eg: commit 1 in master and another commit in a branch, then _git push origin master_ while in any other branch will only push the commits made in master branch..
Any edits made in any branch wont affect pushing of changes made in master.

_git push_ is respective to a particular branch as upstream branch is set.
If want to push a branch while in another branch, given commits are made in the branch to be pushed, then _git push origin branch_ should be done.

**To sum up pushing**:

* _git push origin branch-name_ will push _branch-name_ branch from any branch if commits are made in _branch-name_ branch.
* If remote branch _branch-name_ is not present or created, then _git push origin branch-name_ will automatically create branch _branch-name_.
* _git push -u origin branch-name_ is used to set upstream branch so _git push_ can be used. If branch doesn't exist in remote, then -u can be used in first push as well. **Note: Once upstream is set, _git push_ will be for the current working branch. It is specific to local branch. Upstream is for local branch to understand where to push in remote when just using _git push_**
* _git push_ can be used. But is specific to local branch because of upstream.

