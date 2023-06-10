---
layout: default
title: Auto-Login SSH (Mac) 
parent: SLURM
grand_parent: Terminal
---

# Login with no password

On your computer, run the following:

```
ssh-keygen -t rsa -b 4096
```
<br />

**NOTE:** Do not set a passphrase when creating the key (Press enter 3 times). Make sure that this file is only readable by you! The public key file (id_dsa.pub or id_rsa.pub) as the name implies can be uploaded to other systems to which you would like passwordless access.

Now, create a `~/.ssh` directory on the cluster (doesn't matter if this is already there).

```
ssh <username>@schooner.oscer.ou.edu mkdir -p .ssh
```
<br />

Append the public key to the cluser and enter password one last time:

```
cat .ssh/id_rsa.pub | ssh <username>@schooner.oscer.ou.edu 'cat >> ~/.ssh/authorized_keys'
```
<br />
