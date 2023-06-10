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

## B. Prepare the following input file,`tleap.in`, for *tleap*

```
source leaprc.protein.ff19SB
source leaprc.water.opc

ramp=loadpdb RAMP1.pdb

bond ramp.27.SG ramp.82.SG
bond ramp.40.SG ramp.72.SG
bond ramp.57.SG ramp.104.SG

saveAmberParm ramp RAMP1_gas.prmtop RAMP1_gas.inpcrd

addIons ramp Na+ 2

solvateOct ramp OPCBOX 10.0

addIonsRand ramp Na+ 19 Cl- 19

saveamberparm ramp RAMP1_ion.prmtop RAMP1_ion.inpcrd
```

## C. Run *tleap*

```
tleap -sf tleap.in
```

## D. Check output with VMD

*Note:* The position of the ions are random, so yours will look different.

- Load VMD up.=

- Select `File` > `New Molecule`

- Find your `filename`.parm7 and `filename`.rst7. You'll load one of these first, and then the other.