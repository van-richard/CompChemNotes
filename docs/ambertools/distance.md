---
layout: default
title: PyTraj Distance
parent: AmberTools
---

# Distance analysis from trajectory

```
import pytraj as pt
import matplotlib.pyplot as plt

topology = "/directory/topology.parm7"
trajectory = "/directory/file.nc"

traj = pt.load(trajectory, top="topology")
distance = pt.distance(traj, "selection")
plt.plot(distance)
```