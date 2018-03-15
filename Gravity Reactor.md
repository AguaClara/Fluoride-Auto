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
# Q.to(u.m*u.m*u.m/u.s)
D=(1/8)*u.inch
# D.to(u.m)
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


Qpacl=.00475*(u.milliliter)/(u.second)
Qpacl.to(u.m*u.m*u.m/u.s)
Dpacl=.000508*(u.m)
#Use microbore inner diameter of 1/50 inches
Apacl=np.pi*Dpacl*Dpacl/4
print(Apacl)
vpacl=Qpacl/Apacl
print(vpacl)
headP=.05*(u.meter)
# I believe that the headP should be the difference between where the coagulant line meets the water and fluoride line, because that gives us the input velocity into the "system". This is based on an understanding of plug flow reactors and how we deal with the inputs of secondary flows into the system. However, this may raise an issue because of the fact that the entire system is connected. I believe that we can model the additional inputs into the plug flow system (like a river, for example) with additive flows because it is acting like a sort of drip system. Is there some sort of "ghost pressure" or something that would inhibit our flow into the system in the T-joint connecting the water and the coagulant lines? Also, what is driving the flow of coagulant? How can we assume the input as being relative to the T-joint when it is likely relative to the effluent just like the water constant head tank is? Is the solution instead to model the flows in our system as constant and relative to the effluent, similar to that of how we modeled the water flow?

Lpacl=headP*g*Dpacl*Dpacl/32/vis/vpacl
# Lpacl.to(u.m)
print(Lpacl.to(u.m))
#fricfactor=(64*vis.to(u.m*u.m/u.s))/(v.to(u.m/u.s)*D.to(u.m))
#print(fricfactor)
#h2 = fricfactor * (8/(g*np.pi*np.pi))*(L*Q.to(u.m*u.m*u.m/u.s)**2)/(D.to(u.m)**5)
#print(h2)
Q_pacl_arr = [0.00475, 0.0095, 0.019, 0.038]*u.mL/u.s
v_pacl_arr = Q_pacl_arr/Apacl


deltah2=((v**2)/2/g+hf).to(u.m)
print(deltah2)
```
