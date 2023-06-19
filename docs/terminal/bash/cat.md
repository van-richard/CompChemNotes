---
layout: default
title: cat
grand_parent: Terminal
parent: BASH
---

# Use `cat` to print files to stdout:

```
cat file.txt
```

We can also read the file using `cat`:

```
Contents=$(cat file.txt)
```

- "\n" prints a new line character
- "-e" to interpret the new line escape characters as escape characters

```
echo -e "START OF FILE\n$Contents\nEND OF FILE"
```
