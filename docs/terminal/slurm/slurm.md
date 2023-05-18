---
layout: default
title: SLURM 
parent: Terminal
has_children: true
---

Examples shown below references the OSCER Supercomputer at the University of Oklahoma. However, this similar commands can be used for other supercomputers with minor adjustments.

NOTE: Change `<username>` with your supercomputing account name.

## Table of Content

1. [Login](#Login)
2. [Submitting Jobs](#Submitting-Jobs)
3. [SLURM Queue](#checking-slurm-queue)
4. [Node Information](#get-node-information)
5. [Download Files/Folders](#download-filesfolders)
6. [Upload Files/Folders](#uploading-filesfolders)

## Login 

OSCER has 2 login nodes, if you don't specify which of the two, then it will automatically chose on for you.

```
ssh <username>@schooner.oscer.ou.edu    # Auto
```
```
ssh <username>@schooner1.oscer.ou.edu   # Login Node 1
```
```
ssh <username>@schooner2.oscer.ou.edu   # Login Node 2
```  
<br />

## Submitting Jobs

To submit jobs to the SLURM scheduler, use `sbatch` followed by the name of your batch script.

```
sbatch script.slurm
```
<br />

### SLURM flags

| Option                  | Meaning |
| :-----                  | :------ |
| \--partition=NAME       | Job to run on partition "NAME" |
| \--time=HH:MM:SS        | Amount of wall time requested for job (Hours:Minutes:Seconds) | 
| \--nodes=#              | Number of nodes to use |
| \--ntasks=#             | Number of tasks (processors) to be run |
| \--cpus\-per\-task=#    | Number of CPUs required for each task (e.g. '8' for an 8-way multithreaded job) |
| \--ntasks\-per\-core=1  | Do not use hyperthreading (this flag typically used for parallel jobs) | 
| \--mem=#g               | Memory required for the job (Note the g (GB) in this option) |
| \--exclusive            | Allocate the node exclusively |
| \--error=%j.err         | JOBID as name of stderr file (by default, slurm######.out in the submitting directory) | 
| \--output=%j.out        | JOBID as name of stdout file (by default, slurm######.out in the submitting directory) | 
| \--job\-name=NAME       | Name your job, "NAME", so you can identify it in the queue |
| \--array=0-#            | Mechanism for submitting and managing similar jobs (# can be index values) |

### Example

Example of debug batch script.

```
#!/bin/bash
#SBATCH --partition=debug
#SBATCH --nodes=1
#SBATCH --ntasks=1
#SBATCH --mem=1g
#SBATCH --output=%j.out
#SBATCH --error=%j.err
#SBATCH --time=00:05:00
#SBATCH --job-name=example
```
<br />

## Checking SLURM queue 

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

## Linux/Mac

If your OS is Linux/Mac, login is straight forward (`<username>` is your username): 

```
ssh <username>@schooner.oscer.ou.edu 
```
<br />

