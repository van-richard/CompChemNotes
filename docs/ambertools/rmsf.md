---
layout: default
title: RMSD
parent: AmberTools
---

# Root Mean Squared Deviation

```
import pytraj as pt
import matplotlib.pyplot as plt
import sys

topology = "/directory/topology.parm7"
trajectory = "/directory/file.nc"

traj = pt.load(trajectory, top="topology")

pt.superpose(traj, ref=0)
rmsf = pt.rmsf(traj)
lab = 'Replica ' + rep[j]
plt.plot(rmsf.T[0], rmsf.T[1], label=lab)

# Label Domains based on Residue Number
plt.axvspan(   1,   56, facecolor='tab:red', alpha=0.2, label='RuvC')
plt.axvspan( 718,  765, facecolor='tab:red', alpha=0.2)
plt.axvspan( 925, 1102, facecolor='tab:red', alpha=0.2)
plt.axvspan(  56,  718, facecolor='tab:blue', alpha=0.2, label='Rec')
plt.axvspan( 765,  924, facecolor='tab:orange', alpha=0.2, label='HNH')
plt.axvspan(1099, 1368, facecolor='tab:green', alpha=0.2, label='PAM')

plt.xlabel('Residue #')
plt.ylabel('Distance ($\AA$)')
plt.ylim(0,7)
plt.title(labels[i])
plt.legend(loc=2)
plt.savefig('img/'+folders[i]+'rmsf.png', dpi=300)
```
