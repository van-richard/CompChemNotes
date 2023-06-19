---
layout: default
title: grep
grand_parent: Terminal
parent: BASH
---

# grep - Searching for Pattern in File/Folders.

## Example

```
grep [OPTIONS] 'PATTERN' FILE
```

## Search pattern ignoring case

```
grep -i PATTERN FILE
```

## Search pattern and get NEXT NUMBER of lines

```
#grep -A NUMBER PATTERN FILE
```

## Search pattern and get previous NUMBER of  lines

```
grep -B NUMBER PATTERN FILE
```