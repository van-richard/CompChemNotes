---
layout: default
title: Rock Movie
parent: ChimeraX
---

# Rocking the View in a Movie

## The code looks like 

```
movie record supersample 3
rock y 25 360
wait 360
movie encode ~/Desktop/movie.mp4
```

Where:

movie record [options] - begins the screen recording, addition option `supersample 3`
rock [axix] [degree] [frame #] - rock along the `y`-axis, moving `25` degree along the axis for `360` frames
wait [frame] - number of wait-frames before running the next line
movie encode [location] - save the video at specified location

