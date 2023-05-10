---
layout: default
title: Conda Commands
parent: Python
---

# Conda Commands

Creating a new virtual environment.

```
conda create -n <name>                          # Create New environment
conda create -n <name> python=<version-number>  # Specific Python version
```
<br />
Running the new environment.

```
conda activate <name>
```
<br />
In your new activated environment, you can now install needed packages.

```
conda install <package-name>                 # Install Package
conda install -c conda-forge <package-name>  # Install package from a specific channel (-c)
```
<br />
To leave a virutal environment.

```
conda deactivate
```
<br />
Deleting conda environments and related packages.

```
conda env remove -n <name>
```
<br />
List available environments.

```
conda env list
```
<br />
List packages within an environment.

```
conda activate <name>
conda list
```
<br />
Exporting environments to a YML file.

```
conda activate <name>
conda env export > <name>.yml
```
<br />
Installing a Conda environment from a YML file.

```
codna env create -f <name>.yml
```
<br />

### Example with AmberTools

```
conda create -n ambertools
conda activate ambertools
conda install -c conda-forge ambertools=22 compilers
```
<br />

### Intel Environments on m1/m2 Macs

Intel Conda environment on m1/m2 Macs. Ambertools example.

```
CONDA_SUBDIR=osx-64 conda create -n ambertools python=3.10
conda activate ambertools
python -c "import platform;print(platform.machine()) "
conda env config vars set CONDA_SUBDIR=osx-64
conda deactivate
conda activate ambertools
```
<br />
