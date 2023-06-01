---
layout: default
title: Distances
parent: AmberTools
---

# Distance analysis from trajectory

Plotting distances between `selection`. Which can be Amber mask.

```
import pytraj as pt
import matplotlib.pyplot as plt

topology = "/directory/topology.parm7"
trajectory = "/directory/file.nc"

traj = pt.load(trajectory, top="topology")
distance = pt.distance(traj, "selection")
plt.plot(distance)
```