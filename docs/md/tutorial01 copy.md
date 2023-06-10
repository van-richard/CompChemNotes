---
layout: default
title: Tutorial 1 
parent: Molecular Dynamics
# nav_order: 2
---

# Building Protien Systems in Explicit Solvent

Modified tutorial from [Amber MD](https://ambermd.org/tutorials/basic/tutorial7/index.php) by Abigail Held and Maria Nagan.

Follow everything up to section **IV. Use LEaP to Build a Protein System in Explicit Solvent**

## A. Set AMBERHOME

To run an executable in Amber, you need set the AMBERHOME environment variable. This script will set up your shell environment for that:

```
source /home/van/.Programs/amber20/amber.sh
```

## B. Prepare the following input file,`tleap.in`, for *tleap