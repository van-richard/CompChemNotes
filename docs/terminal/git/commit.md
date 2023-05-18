---
layout: default
title: commit 
parent: Git
grand_parent: Terminal
---
 
# Commit with a message

```
git commit -m "Added multiplyNumbers() function to HelloWorld.c"
```

## Signed commit with a message (user.signingkey must have been set with your GPG key e.g. git config --global user.signingkey 5173AAD5)

```
git commit -S -m "signed commit message"
```

## Automatically stage modified or deleted files, except new files, and then commit

```
git commit -a -m "Modified foo.php and removed bar.php"
```

## Change last commit (this deletes previous commit with a fresh commit)

```
git commit --amend -m "Correct message"
```
