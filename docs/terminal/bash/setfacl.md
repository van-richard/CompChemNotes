---
layout: default
title: setfacl
grand_parent: Terminal
parent: BASH
---

# Give specific user permission to read/write/execute a folder.

`setfacl` is short for set File ACL (Access Control List). This sets permissions for specific users, without changing the owndership of the directory.

```
setfacl -m u:username:rwx myfolder
```

# Options 

Helpful options.

| Option | Meaning |
| :----- | :------ |
| \-m, \--modify=acl        | modify the current ACL(s) of file(s) |
| \-M, \--modify-file=file  | read ACL entries to modify from file |
| \-x, \--remove=acl        | remove entries from the ACL(s) of file(s) |
| \-b, \--remove-all        | remove all extended ACL entries |
| \-R, \--recursive         | recurse into subdirectories |
