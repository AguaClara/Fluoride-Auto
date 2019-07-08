```python
import math as m
import numpy as np
from aguaclara.play import*

#UPFLOW VELOCITY
#Cross-sectional area of
A_reactor = 506.7*u.mm**2
#Input height of effluent tube
H_effluent = 2.5 * u.cm
#Volumetric flow rate
#Slope of the graph from Spring 2019
Slope_effluent = 0.028778 * u.mL/u.s/u.cm
Q_reactor = H_effluent * Slope_effluent
Q_reactor = Q_reactor.to(u.mm**3/u.s)
#Upflow Velocity
V_up = Q_reactor/A_reactor
print("Upflow velocity is "+str(V_up))

#PACL CONCENTRATION
#Concentration of PACl stock
C_stock_PACl = 1000 * u.mg/u.L
#Input height of PACl adjustable maneuver
H_PACl = 6 * u.cm
#Volumetric flow rate
#Slope of the graph from Spring 2019
Slope_PACl = 0.000544 * u.mL/u.s/u.cm
Q_stock_PAC = H_PACl * Slope_PACl
C_stock_PAC = 1000 * u.mg/u.L
C_stock_PAC = C_stock_PAC.to(u.mg/u.mL)
C_reactor_PAC = Q_stock_PAC*C_stock_PAC/(Q_reactor.to(u.L/u.s))
print("Concentration of PACl in the reactor is "+str(C_reactor_PAC))
