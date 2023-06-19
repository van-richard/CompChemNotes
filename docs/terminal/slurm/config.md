---
layout: default
title: ssh config File 
parent: SLURM
grand_parent: Terminal
---

# Managing Multiple SSH Connections

If you are regularly connecting to multiple remote systems over SSH, you’ll find that remembering all of the remote IP addresses, different usernames, non-standard ports, and various command-line options is difficult.

OpenSSH allows you to set up a per-user configuration file, `~/.ssh/config`, where you can store different SSH options for each remote machine you connect to.

Make a `~/.ssh/config` file, and include the following:

```
Host ALIAS1
    HostName <hostname1>
    User <username1>

Host ALIAS2
    HostName <hostname2>
    User <username2>

Host ALIAS3
    SSH_OPTION value
    SSH_OPTION value
```

- `ALIAS` would some pattern for your login (i.e. `ssh ALIAS1`).
- `HostName` is the <hostname> without the `@`.
- `User` is only your <username>.
- NOTE: Indentations are not required, but makes the file easier to read.

