---
layout: default
title: awk
grand_parent: Terminal
parent: BASH
---

# AWK - Manipulation of text!

Treating a text file, were each space is a column, you can print the columns with:

```
awk '{print $1}' file
```

Where `$1` is the first column. Index starts at 1.

## Separator

You can chose the field separator with, `-F`. This example choses the comma as the separator, and print the 5th column:

```
awk -F ',' '{print $5} file'
```

## MATH

### Averager a column

```
awk '{ total += $2; count++ } END { print total/count }' file
```
