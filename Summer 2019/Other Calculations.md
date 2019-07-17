```python
#Convert RPM back to mL/s or mg/L (in case there were calculation errors) - can also use for calculating concentration in gravity system
#WATER
Q_tap_rpm = 39 /u.minute
Q_reactor = Q_tap_rpm*water_tube/(60*u.sec/u.minute)
print('Water in mL/s is: '+str(Q_reactor))

#PACL
#RPM from the pump
PAC_rpm = 92*u.turn/u.minute
stock_PAC = PAC_rpm*oy_tube/(60*u.sec/u.minute)
stock_PAC=0.0120*u.mL/u.sec
reactor_PAC = stock_PAC*(C_stock_PACl/Q_reactor)
print('PACl concentration is: '+str(reactor_PAC))

#FLUORIDE
#RPM from the pump
fluoride_rpm =
stock_fluoride = fluoride_rpm*oy_tube/(60*u.sec/u.minute)
reactor_fluoride = stock_fluoride*(C_stock_fluoride/Q_reactor)
print('Fluoride concentration is: '+str(reactor_fluoride))
```
