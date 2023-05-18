---
layout: default
title: push 
parent: Git
grand_parent: Terminal
---
 
# Push and merge changes from a local repo to remote named "origin" and "master" branch.

```
git push <remote> <branch>
git push origin master
```

## By default, git push will push and merge changes from the current branch to its remote-tracking branch

```
git push
```

## To link up current local branch with a remote branch, add -u flag:

```
git push -u origin master
```

## Now, anytime you want to push from that same local branch, use shortcut:

```
git push
```
