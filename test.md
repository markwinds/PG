---
markdown:
  image_dir: /assets
  path: output.md
  ignore_from_front_matter: true
  absolute_image_path: false
--- 

[TOC]

# test

```python {cmd=python3 matplotlib=true numpy=true }
import matplotlib.pyplot as plt
plt.plot([1,2,3, 4])
plt.show() # show figure
```


# yu

```gnuplot {cmd=true output="html" hide}
set terminal svg
set title "Simple Plots" font ",20"
set key right box
set samples 500
set style data points

f(x)=x**3

plot f(x),x**4
```