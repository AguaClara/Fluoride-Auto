$$ P_1 + \rho g \Delta h_1+ \frac{1}{2}\rho {v_1}^2 = P_2 + \rho g \Delta h_2+ \frac{1}{2}\rho {v_2}^2+ h_f $$

We can cancel out our pressure teams since the inflow and outflow are both to the atmosphere, as well as the velocity at point 1 since the constant head valve guarantees no change in velocity in this tank. Therefore the Bernoulli equation becomes the following:
$$ \rho g \Delta h_1 = \rho g \Delta h_2+ \frac{1}{2}\rho {v_2}^2+ h_f
$$
We can input our known variables for Volumetric Flow (Q), Area of our tubes (A), the gravitational constant (g), and $h_1$ as our reference point making it zero.
$$ Q= .76 * {10}^-6 \frac{{m}^3}{s}$$
$$ g = 9.8 \frac{m}{{s}^2} $$
$$ d = \frac {3}{16} in * 2.54 \frac {cm}{in} * \frac {1 m}{100 cm} $$
$$ A = \pi * {(\frac {d}{2})^2}$$
$$ v = \frac{Q}{A} $$

Resulting in this equation:

$$ \Delta h_2 = \frac {\frac{v^2}{16}}{2g} + h_f $$
%$$ \Delta h_2 = \frac {.04266 \frac{m}{{s}^2}}{2*g}$$
$$ h_f = \frac {L}{v} * \nu * \frac{G_{coil}^2}{g} $$
$$ \nu = \frac{\mu}{\rho} = 8.9861*10^-7 \frac{m^2}{s}$$
$$ L = 9.43m $$
$$ G_{coil} = $$

$$ \Delta h = h_f + h_2 $$



Using the same principle as the water flow, we can calculate the height difference we would need for a correct flow of coagulant.

```python
import math as m
import numpy as np
from aide_design.play import*
import aide_design.floc_model as fm

Q=.76*(u.milliliter)/(u.second)
Q.to(u.m*u.m*u.m/u.s)
D=(1/8)*u.inch
D.to(u.m)
A=np.pi*(D**2)/4
print(A)
v=(Q/A).to(u.m/u.s)
print(v)
L=9.43*u.m
T = 298 * u.degK
vis = pc.viscosity_kinematic(T)
print(vis)
Gcoil=206.907*(1/u.s)
g=9.81*(u.meter)/(u.second)/(u.second)
hf=((Gcoil**2)*vis*L/v/g).to(u.m)
print(hf)
R_c = 0.05*u.m
shearG = fm.g_coil(Q,D,R_c,T)
print(shearG)
hfModel=((shearG**2)*vis*L/v/g).to(u.m)
print(hfModel)
#fricfactor=(64*vis.to(u.m*u.m/u.s))/(v.to(u.m/u.s)*D.to(u.m))
#print(fricfactor)
#h2 = fricfactor * (8/(g*np.pi*np.pi))*(L*Q.to(u.m*u.m*u.m/u.s)**2)/(D.to(u.m)**5)
#print(h2)

deltah2=((v**2)/2/g+hf).to(u.m)
print(deltah2)
```
