---
layout: default
title: if
grand_parent: Terminal
parent: BASH
---

# Condition is true if the value of $name is not equal to the current user's login username:

```
if [[ "$name" != "$USER" ]]; then
    echo "Your name isn't your username"
else
    echo "Your name is your username"
fi
```

# To use && and || with if statements, you need multiple pairs of square brackets:

```
read age
if [[ "$name" == "Steve" ]] && [[ "$age" -eq 15 ]]; then
    echo "This will run if $name is Steve AND $age is 15."
fi

if [[ "$name" == "Daniya" ]] || [[ "$name" == "Zach" ]]; then
    echo "This will run if $name is Daniya OR Zach."
fi
```

# There are other comparison operators for numbers listed below:

```
# -ne - not equal
# -lt - less than
# -gt - greater than
# -le - less than or equal to
# -ge - greater than or equal to
```

# There is also the `=~` operator, which tests a string against the Regex pattern:

```
email=me@example.com
if [[ "$email" =~ [a-z]+@[a-z]{2,}\.(com|net|org) ]]
then
    echo "Valid email!"
fi
```