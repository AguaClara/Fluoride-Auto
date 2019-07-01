```python
import math as m
import numpy as np
from aguaclara.play import*

#UPFLOW VELOCITY
#Cross-sectional area of
A_reactor = 506.7*u.mm**2
#Height of effluent tube
H_effluent = 2.5 * u.cm
#Volumetric flow rate
#Slope of the graph developed from volumetrically determining effluent flow rates at different heights
#Slope_effluent =
#Q_reactor =

Q_reactor = (0.76 * u.mL/u.sec).to(u.mm**3/u.sec)
#Upflow Velocity
V_up = Q_reactor/A_reactor

#PACL CONCENTRATION
#Concentration of PACl stock
C_stock_PACl = 1000 * u.mg/u.L
#Volumetric flow rate
#Slope of the graph developed from volumetrically determining PACl flow rates at different heights
#Slope_PACl =
Q_stock_PAC = 


#Slope of PACl: 0.000544 mL/s /cm
#Slope of upflow velocity: 0.028778 mL/s /cm
##Get new data from the grav system for more accurate heights and stuff
