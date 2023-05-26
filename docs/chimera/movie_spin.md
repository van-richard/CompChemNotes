---
layout: default
title: Spin Movie
parent: ChimeraX
---

# Spinning the PDB in a Movie

## The code looks like 

```
movie record supersample 3
turn y 1 360
wait 360
movie encode ~/Desktop/movie.mp4
```

Where:

movie record [options] - begins the screen recording, addition option `supersample 3`
turn [axis] [degree] [frame #] - spin on the `y`-axis at `1` degree every `360` frames
wait [frame] - number of wait-frames before running the next line
movie encode [location] - save the video at specified location

