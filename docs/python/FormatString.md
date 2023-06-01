---
layout: default
title: Format String
parent: Python
---

# Placeholder Zeros for Windows (% Operator)

`%02d` means: Print the interger and if it's shorter than 2 digits, prefix with zeros.

```
for i in range(10):
    window = np.loadtxt('../%02d/step6.00_equilibration.cv' % i)
```

# Printing Floats (% Operator)

`%.3f` means: Print float to 3 decimal places

```
val = np.linspace(0,1,10)
for i in val:
    print('The value is %.3f' % i)
```

# String Formatting (str.format)

```
name = Richard
'Hello, {}.format(name)'
```

# String Interpolation aka f-Strings 

```
name = Richard
f'Hello, {name}'
```

or 

```
a = 5
b = 10
f'Five plus ten is {a + b} and not {2 * (a + b)}.'
```