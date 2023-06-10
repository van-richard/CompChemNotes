---
layout: default
title: Molecular Dynamics 
nav_order: 7
has_children: true
---

# Overview

## Prepare Amber Inputs with tleap (parm7, rst7)

To start running simulations with Amber, you'll need to prepare 2 files, 1) `filename`.parm7, and 2) `filename`.rst7. 

### `filename`.parm7

Is a parameter file, containing all the atomic parameters for your system.

### `filename`.rst7 

Is a restart file, containing all the atomic coordinates for your system.

# Equilibrating your system

After you have prepared you parameter/topology files, we'll need to run the following:

1. Minimization
2. Heating
3. Density

