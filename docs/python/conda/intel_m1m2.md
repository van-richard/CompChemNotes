---
layout: default
title: Intel Env. on Apple Silicon
grand_parent: Python
parent: Conda
---

# Intel Environments on m1/m2 Macs

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
