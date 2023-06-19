---
layout: default
title: cp
grand_parent: Terminal
parent: BASH
---

# Copy files/folders

Copy file1 to file2 (new name):

```
cp [FILE_1] [FILE_2]
```

Copy folders:

```
cp -r [FOLDER_1] [FOLDER_2]
```

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

## Copying can be down with paths

```
cp -r /path/to/dir_1 /path/to/dir_2
```
