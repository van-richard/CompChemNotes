---
layout: default
title: Upload Files/Folders
parent: SLURM
grand_parent: Terminal
---

# Uploading Files/Folders

The commands `scp` and `rsync` also uploads files and folders, just switch the [source] and [destination].

```
scp file <username>@schooner.oscer.ou.edu:/path/to/file                  # File Upload
```
```
scp directory <username>@schooner.oscer.ou.edu:/path/to/directory        # Folder Upload
```
<br />
```
rsync -avuim file <username>@dtn2.oscer.ou.edu:/path/to/file         # File Upload
```
```
rsync -avuim folder <username>@dtn2.oscer.ou.edu:/path/to/directory  # Folder Upload
```
<br />
