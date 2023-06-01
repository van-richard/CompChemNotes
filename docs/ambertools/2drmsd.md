---
layout: default
title: 2D-RMSD
parent: AmberTools
---

# Root Mean Squared Deviation

```
import pytraj as pt
import matplotlib.pyplot as plt

topology = "/directory/topology.parm7"
trajectory = "/directory/file.nc"

traj = pt.load(trajectory, top="topology")

mat = pt.pairwise_rmsd(traj)

im = plt.imshow(mat, cmap='jet',vmax=3.0)

plt.colorbar(im, fraction=0.046, pad=0.04, label='RMSD ($\AA$)')
plt.title(labels[i] + ' ' + rep[j])
plt.xlabel('Frame #')
plt.ylabel('Frame #')
plt.gca().invert_yaxis()
plt.tight_layout()
plt.savefig('img/'+folders[i]+rep[j]+'2drmsd.png', dpi=300)   
```
