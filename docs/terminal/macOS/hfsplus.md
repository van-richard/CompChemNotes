---
layout: default
title: HFS+
grand_parent: Terminal
parent: macOS
---

# HFS+ is the file system used by many Apple computers with MacOS. 

This filesystem can be mounted in Ubuntu with read only access by default. If you need read/write access, then you need to disbale journaling with OS X before you can continue.

In OS X, open terminal and run the following to find partition identifier:

```
diskutil list
```

Find the volume name of the partition under, `NAME`.

Then you can run the following:

```
sudo diskutil disableJournal <volume_name>
```

To re-enable journaling:

```
sudo diskutil enableJournal <volume_name>
```

