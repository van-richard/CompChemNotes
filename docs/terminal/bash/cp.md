---
layout: default
title: cp
grand_parent: Terminal
parent: BASH
---

# Copy files/folders

Use `cp` to copy files or directories from one place to another.

- `cp` creates NEW versions of the sources, so editing the copy won't affect the original (and vice versa).
## Note that it will overwrite the destination if it already exists.

```
cp srcFile.txt clone.txt
```

or

```
cp -r srcDirectory/ dst/ # recursively copy
```
