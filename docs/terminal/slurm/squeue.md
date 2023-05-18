---
layout: default
title: squeue (Checking Jobs) 
parent: SLURM
grand_parent: Terminal
---

# Checking SLURM queue 

Shows all jobs running/pending in queue.

```
squeue 
```
<br />
Show *your* jobs that are running/pending in queue.

```
squeue -u <username> 
```
<br />
Find running/pending jobs for a specific partition.

```
squeue -p <ParitionName>
```
<br />