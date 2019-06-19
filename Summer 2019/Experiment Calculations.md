```python
import math as m
import numpy as np
from aguaclara.play import*

#UPFLOW VELOCITY
#Diameter of reactor tube
D_reactor = 1 * u.inch
#Input upflow velocity
V_up = 1 * u.mm/u.s
#Flow rate into reactor
Q_reactor = (m.pi*((D_reactor/2)**2)*V_up).to(u.mL/u.s)
#Height of reactor
H_reactor = 50 * u.inch
# Volume of reactor
Vol_reactor = (m.pi * ((D_reactor)**2)*H_reactor/4).to(u.mL)
# Residence time in reactor
T_residence= (Vol_reactor/Q_reactor).to(u.minute)

#PACL
#Concentration of PACl stock
C_stock_PACl = 1000*u.mg/u.L
#Input concentration of PACl that you want in the reactor
C_reactor_PAC = 25*u.mg/u.L
#Coagulant microtubing (orange-yellow)
oy_tube=0.019*u.mL/u.revolutions
#Flow rate of PACl in mL/s (put into ProCoDA)
Q_stock_PAC = Q_reactor*(C_reactor_PAC/C_stock_PACl)
print('PACl should be set in ProCoDA to: '+ str(Q_stock_PAC))
Q_stock_PAC_rpm = (Q_stock_PAC/oy_tube)*60*u.sec/u.min
print('PACl in rpm is: '+str(Q_stock_PAC_rpm))

#FLUORIDE
#Concentration of fluoride stock
C_stock_F = 1000*u.mg/u.L
#Input concentration of fluoride that you want in the reactor
C_reactor_F = 5*u.mg/u.L
#Fluoride microtubing (orange-yellow)
oy_tube=0.019*u.mL/u.revolutions
#Flow rate of fluoride in mL/s (check in ProCoDA)
Q_stock_F = Q_reactor*(C_reactor_F/C_stock_F)
print('Fluoride can be set in ProCoDA to: '+str(Q_stock_F))
#Flow rate of fluoride in RPM (put into manual pump)
Q_stock_F_rpm = (Q_stock_F/oy_tube)*60*u.sec/u.min
print('Fluoride pump should be set at: '+str(Q_stock_F_rpm))

#WATER
#Flow rate of water in mL/s (put into ProCoDA)
Q_tap = Q_reactor - 1*Q_stock_PAC - 1*Q_stock_F
print('Water should be set in ProCoDA to: '+str(Q_tap))
water_tube = 0.8*u.mL/u.revolutions
Q_tap_rpm = (Q_tap/(water_tube))*(60*u.sec/u.minute)
print('Water in rpm should be: ' + str(Q_tap_rpm))
