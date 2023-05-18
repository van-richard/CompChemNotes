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
cat .ssh/id_rsa.pub | ssh <username>@schooner.oscer.ou.edu `cat >> ~/.ssh/authorized_keys`
```
<br />

---
layout: default
title: Automatic SSH
parent: Terminal
---

# Automatic SSH (No Password) for MacOS

Generate a key in your `/home/`:

```
# -t is type
# -b is bits
ssh-keygen -t rsa -b 4096
```

Save the key in the default, it should be `~/.ssh/id_rsa`. You do not want to have a passphrase. Press enter 3 times. 

Congrats! You now have a key! Two files are made: 

1. id_rsa - This is your RSA "private" key used to sign and authenticate your connection to a remote host.
2. id_rsa.pub - This is your "public" key, which when suppied to the remote host (Next step), allows the host to authenticate the connections as being from you.

Copy the key to your remote host (i.e. Schooner, PETE, etc.), by adding this to the `authorized_keys` file.

```
cat ~/.ssh/id_rsa.pub | ssh <username>@<hostname> 'cat >> ~/.ssh/authorized_keys'
```

Enter your password one last time, and you're done!
