---
layout: default
title: Plotting
parent: Python
---

# Plotting with matplotlib.pyplot

```
import matplotlib.pyplot as plt
```

# Example

```
import matplotlib.pyplot as plt
import numpy as np

xpoints = np.array([1, 8])
ypoints = np.array([3, 10])

plt.plot(xpoints, ypoints)
plt.show()
```

# Multiple Plots in one Figure

```
import matplotlib.pyplot as plt
import numpy as np

# Some example data to display
x = np.linspace(0, 2 * np.pi, 400)
y = np.sin(x ** 2)

fig, ax = plt.subplots()
ax.plot(x, y)
ax.set_title('A single plot')
```

# Vertical Subplots

```
import matplotlib.pyplot as plt
import numpy as np

# Some example data to display
x = np.linspace(0, 2 * np.pi, 400)
y = np.sin(x ** 2)

fig, axs = plt.subplots(2)
fig.suptitle('Vertically stacked subplots')
axs[0].plot(x, y)
axs[1].plot(x, -y)
```

# Horizontal Subplots

```
import matplotlib.pyplot as plt
import numpy as np

# Some example data to display
x = np.linspace(0, 2 * np.pi, 400)
y = np.sin(x ** 2)

fig, ax = plt.subplots(1, 2)
fig.suptitle('Horizontally stacked subplots')
ax[0].plot(x, y)
ax[1].plot(x, -y)
```

# 2x2 Subplot

```
import matplotlib.pyplot as plt
import numpy as np

# Some example data to display
x = np.linspace(0, 2 * np.pi, 400)
y = np.sin(x ** 2)

fig, ax = plt.subplots(1, 2)
fig.suptitle('Horizontally stacked subplots')
ax[0,0].plot(x, y)
ax[0,1].plot(x, y)
ax[1,0].plot(x, -y)
ax[1,1].plot(x, -y)
```