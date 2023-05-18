---
layout: default
title: pull 
parent: Git
grand_parent: Terminal
---
 
# Update your local repo, by merging in new changes from the remote "origin" and "master" branch.

```
git pull <remote> <branch>
git pull origin master
```

## By default, git pull will update your current branch by merging in new changes from its remote-tracking branch

```
git pull
```

## Merge in changes from remote branch and rebase branch commits onto your local repo, like: "git fetch <remote> <branch>, git rebase <remote>/<branch>"

```
git pull origin master --rebase
```