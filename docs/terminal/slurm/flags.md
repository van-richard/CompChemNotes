---
layout: default
title: SLURM Flags 
parent: SLURM
grand_parent: Terminal
---

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