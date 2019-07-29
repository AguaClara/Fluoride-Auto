```python
import math as m
import numpy as np
from aguaclara.play import*

#Convert flow rate into upflow velocity
D_reactor = (1*u.inch).to(u.mm)
A_reactor = m.pi*(D_reactor/2)**2
Q_reactor = 0.787 * u.mL/u.sec
V_up = Q_reactor / (A_reactor*0.001*u.mL/u.mm**3)
print("Upflow velocity is "+str(V_up))

#Convert upflow velocity into flow rate
v_up = 1.55 * u.mm/u.sec
q_reactor = v_up * (A_reactor*0.001*u.mL/u.mm**3)
print("Flow rate is "+str(q_reactor))

#Convert RPM back to mL/s or mg/L (in case there were calculation errors) - can also use for calculating concentration in gravity system
#WATER
Q_tap_rpm = 39 /u.minute
Q_reactor = Q_tap_rpm*water_tube/(60*u.sec/u.minute)
print('Water in mL/s is: '+str(Q_reactor))

#PACL
#RPM from the pump
C_stock_PACl = 1000 * u.mg/u.L
Q_reactor = 0.787 * u.mL/u.sec
#PAC_rpm = 92*u.turn/u.minute
#stock_PAC = PAC_rpm*oy_tube/(60*u.sec/u.minute)
stock_PAC=0.01377*u.mL/u.sec
reactor_PAC = stock_PAC*(C_stock_PACl/Q_reactor)
print('PACl concentration is: '+str(reactor_PAC))

#FLUORIDE
#RPM from the pump
fluoride_rpm =
stock_fluoride = fluoride_rpm*oy_tube/(60*u.sec/u.minute)
reactor_fluoride = stock_fluoride*(C_stock_fluoride/Q_reactor)
print('Fluoride concentration is: '+str(reactor_fluoride))
```
