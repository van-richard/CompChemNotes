---
layout: default
title: printf
grand_parent: Terminal
parent: BASH
---

# Format Output

Similar to C/C++, Java, and PHP.

```
printf -v VARIABLE FORMAT ARGUMENTS
```

## Example

Add `1 + 1` as variable `j`.

```
i=1
printf -v j %02d $(( $i + 1 ))
```
