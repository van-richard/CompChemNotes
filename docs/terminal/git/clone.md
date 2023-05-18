---
layout: default
title: clone 
parent: Git
grand_parent: Terminal
---
 
# Clone

``` 
git clone <url>.git
```

## Shallow clone - faster cloning that pulls only latest snapshot

```
git clone --depth 1 <url>.git
```

# Clone only a specific branch

```
git clone -b master-cn <url>.git --single-branch
```
