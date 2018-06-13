#Calculations for Water Pump speed
Calculates RPM of water pump, given a desired upflow velocity in the sedimentation tube.

```python
import math as m
import numpy as np
from aide_design.play import*
import aide_design.floc_model as fm

#Q=.76*(u.milliliter)/(u.second)
#Q.to(u.m*u.m*u.m/u.s)
D=(1)*u.inch
D=D.to(u.m)
A=np.pi*(D**2)/4
print(A)
v=(0.002)*(u.m/u.s)
#Area given our diameter of tubing
Q=(A*v)
print(Q)
Q=Q.to((u.milliliter)/(u.second))
print(Q)
#Manual calculation of RPM
Man_RPM=(Q/((0.8)*(u.milliliter)))
Man_RPM=Man_RPM*(60*(u.second))
print(Man_RPM)

```

#Calculations for Coagulant Pump speed
Calculates RPM of coagulant pump, given a desired concentration in the system.
Assumes flow rate of coagulant pump is negligible compared to the water pump flow rate.

```python

```

#Fluoride pump speed and stock concentration
Calculates volumetric flow rate of fluoride pump, given pump speed in RPM.
Calculates concentration of fluoride in system.
Assumes flow rate of fluoride pump is negligible compared to the water pump flow rate.
Uses tube sizing conversions found on [AguaClara Confluence ](https://confluence.cornell.edu/display/AGUACLARA/Auto+Tutorial+for+Peristaltic+Pumps).

```python
pump_speed = 40*(u.rpm)
yellow_blue = 0.149*(u.milliliter/u.revolutions)
yb_flowrate = yellow_blue.to(u.liter/u.revolutions)*(pump_speed).to(u.revolutions/u.s)
print('The fluoride flow rate is: '+str(yb_flowrate))

fluoride_stock = 1000 * (u.mg/u.L)
v_stock = (280 * u.mL).to(u.L)
v_water = 1 * u.L
total_v = v_water + v_stock
c_solution = (fluoride_stock * v_stock)/(total_v)
print('The fluoride concentration in the stock container is: ' +str(c_solution))

Q_sys = Q.to(u.L/u.s) #water pump speed, calculated above
Q_stock = yb_flowrate
C_stock = c_solution
C_sys = ((Q_stock*C_stock)/(Q_sys)).to(u.mg/u.L)
print('The fluoride concentration in the system is: ' +str(C_sys))

percent_flow = yb_flowrate/Q_sys
print('The percent flow rate of fluoride/total flow through system: '+str(percent_flow))

```
