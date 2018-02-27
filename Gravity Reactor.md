$$ P_1 + \rho g \Delta h_1+ \frac{1}{2}\rho {v_1}^2 = P_2 + \rho g \Delta h_2+ \frac{1}{2}\rho {v_2}^2+ h_f $$

We can cancel out our pressure teams since the inflow and outflow are both to the atmosphere, as well as the velocity at point 1 since the constant head valve guarantees no change in velocity in this tank. Therefore the Bernoulli equation becomes the following:
$$ \rho g \Delta h_1 = \rho g \Delta h_2+ \frac{1}{2}\rho {v_2}^2+ h_f
$$
We can input our known variables for Volumetric Flow (Q), Area of our tubes (A), the gravitational constant (g), and $h_1$ as our reference point making it zero.
$$ Q= .76 * {10}^-6 \frac{{m}^3}{s}$$
$$ g = 9.8 \frac{m}{{s}^2} $$
$$ d = \frac {3}{16} in * 2.54 \frac {cm}{in} * \frac {1}{100} (\frac {m}{cm})$$
$$ A = \pi * {(\frac {d}{2})^2}$$
$$ v = \frac{Q}{A} $$

Resulting in this equation:

$$ \Delta h_2 = \frac {\frac{v^2}{16}}{2g} + h_f $$
%$$ \Delta h_2 = \frac {.04266 \frac{m}{{s}^2}}{2*g}+h_f$$
$$ \Delta h_2 = h_f + .000092756m $$

$$ h_f = $$

```python
import math as m
import numpy as np
from aide_design.play import*

Q=.76*(u.milliliter)/(u.second)
D=(3/16)*u.inch
D.to(u.m)
A=np.pi*(D**2)/4
v=Q/A
G=aide_design.floc_model.g_coil(.76,D,.0381,298)

hL=50*u.centimeter
g=9.80665*(u.meter)/(u.second)/(u.second)
deltah2=((v**2)/2/g+hL).to(u.m)
print(deltah2)
```
