#MathCad Conversions
March 11, 2019

```python
import math as m
from aguaclara.core.units import unit_registry as u
from aguaclara.core import physchem as pc
from aguaclara.core import utility as ut
import numpy as np

#Diameter of reactor tube
D_reactor = 1 * u.inch
#upflow velocity
V_up = 1.5 * u.mm/u.s
#Flow rate into reactor
Q_reactor = (m.pi*((D_reactor/2)**2)*V_up).to(u.mL/u.s)
#Height of reactor
H_reactor = 50 * u.inch
# Volume of reactor
Vol_reactor = (m.pi * ((D_reactor)**2)*H_reactor/4).to(u.mL)
# Residence time in reactor
T_residence= (Vol_reactor/Q_reactor).to(u.minute)



C_stock_PACl = 1000*u.mg/u.L
C_stock_dye = 1000*u.mg/u.L
C_reactor_PAC = 30*u.mg/u.L
C_reactor_F = 5*u.mg/u.L  

Q_stock_PAC = Q_reactor*(C_reactor_PAC/C_stock_PACl)

C_reactor_dye = (Q_stock_PAC*C_stock_dye)/Q_reactor

Q_tap = Q_reactor - 1*Q_stock_PAC
Q_fluoride = (0.5)*Q_tap

C_stock_F = Q_reactor*(C_reactor_F/Q_fluoride)

C_lab_PAC = 70900


#Flocculator Calculations

#Inputs
# flow rate in flocculator
Q_flocculator = Q_reactor
# target G*theta to design the flocculator
Gtheta_goal = 20000
#inner diameter of the flocculator tubing
D_floctube = 0.125 * u.inch
#radius of curvature (the radius of the tube the flocculator is wrapped around)
R_c = 4.25 * u.cm
