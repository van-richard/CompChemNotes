---
layout: default
title: sinfo (Node Info.) 
parent: SLURM
grand_parent: Terminal
---

## Get Node information

List nodes.

```
sinfo
```
<br />
Find all available nodes.

```
sinfo | grep "idle"
```
<br />
Find information on why a specific node is down

```
sinfo -R
```
<br />