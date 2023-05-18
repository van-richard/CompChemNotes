---
layout: default
title: Download Files/Folders 
parent: SLURM
---

## Download Files/Folders

There are 2 options to downloading files and folders.

1. Download with `scp` (Good for small and/or few files/folders) 
    - For files, you will need to be in a second terminal where the _working directory is on your local computer_ and where you want the file to be located
    - For Folders, follow the previous step, and add the flag `scp -r`.
2. Download with `rsync` (For copying large amounts of data, and generally the preferred approach).
    - If a lot of data needs to be transfered it is also preferred to use the data transfer login node on OSCER (dtn2.oscer.ou.edu).
    - Same approach as `scp` but use the flags `rsync -avuim`.
    - `-a` archive - preserve as most of the data.
    - `-v` verbose - print summary of file transfer.
    - `-u` update - only newest file will be kept.
    - `-i` itemize - list of the changes.
    - `-m` prune - delete empty folders.

```
scp <username>@schooner.oscer.ou.edu:/path/to/file .               # File Download
```
```
scp <username>@schooner.oscer.ou.edu:/path/to/directory .          # Folder Download
```
<br />
```
rsync -avuim <username>@dtn2.oscer.ou.edu:/path/to/file .      # File Download
```
```
rsync -avuim <username>@dtn2.oscer.ou.edu:/path/to/directory . # Folder Download
```
<br />