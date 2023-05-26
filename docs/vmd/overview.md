---
layout: default
title: VMD 
nav_order: 6
has_children: true
---

# Optional Customization (Startup File)

In your `/home/<username>`, make a file called `.vmdrc`:

```
menu main on
menu main move 1000 5 

# menu files on
# menu files move 5 575 

menu graphics on
menu graphics move 1200 200 

display resize 1000 1000
display reposition 300 800
display projection orthographic
axes location off
stage location off

color Display Background white
color Labels Bonds black

# turn on lights 0 and 1
light 0 on
light 1 on
light 2 off
light 3 off
```