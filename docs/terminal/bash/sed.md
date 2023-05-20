---
layout: default
title: sed
grand_parent: Terminal
parent: BASH
---

# sed - Tranform text!

We can replace some text, INPUT, with another text, OUTPUT, in a file with `sed`. The notation is:

```
sed 's/INPUT/OUTPUT/' file
```

## Create a new file with replacement

```
sed 's/INPUT/OUTPUT/' file > newfile
```

## Replace occurances within the file

```
sed -i 's/INPUT/OUTPUT/' file
```

## Replace all occurances

```
sed 's/INPUT/OUTPUT/g' file
```

## Delete lines containing pattern

```
sed '/INPUT/d' file
```

## Variables with sed

```
sed "s/INPUT/${VARIABLE}/" file
```

## Multiple inputs

```
sed -e 's/INPUT1/OUTPUT1/;s/INPUT2/OUTPUT2/;s/INPUT3/OUTPUT3/' file
```

