---
layout: default
title: tleap
parent: Molecular Dynamics
---

# Prepare your input files

# Example with Protein, RNA, DNA, and water in Amber20.

```
source leaprc.protein.ff14SB
source leaprc.DNA.OL15
source leaprc.RNA.OL3
source leaprc.water.tip3p 
loadamberparams frcmod.ions234lm_1264_tip3p 

protein = loadpdb prod.pdb

savepdb protein step3_pbcsetup.pdb
charge protein
solvatebox protein TIP3PBOX 12.0 iso 0.8
addions protein Na+ 0

saveamberparm protein step3_pbcsetup.parm7 step3_pbcsetup.rst7
saveamberparm protein step3_pbcsetup.parm7 step3_pbcsetup.ncrst
savepdb protein step3_pbcsetup_wat.pdb

quit
```