```python
import math as m
import numpy as np
from aguaclara.play import*

D=(1)*u.inch
D=D.to(u.m)
A=np.pi*(D**2)/4
print(A)
v=(0.001)*(u.m/u.s)
#Area given our diameter of tubing
Q=(A*v)
print(Q)
Q=Q.to((u.milliliter)/(u.second))
print(Q)
#Manual calculation of RPM
Man_RPM=(Q/((0.8)*(u.milliliter)))
Man_RPM=Man_RPM*(60*(u.second))
print(Man_RPM)

#Aim for 6.5 mg/L of PAC the lowest according to Github Issues
pump_speed_PACl = 80*(u.rpm)
orange_yellow = 0.019*(u.milliliter/u.revolutions)
oy_flowrate_PACl = orange_yellow.to(u.liter/u.revolutions)*(pump_speed_PACl).to(u.revolutions/u.s)

print('The PACl flow rate is: '+str((oy_flowrate_PACl).to(u.milliliter/u.s))) #Qstock

Q_sys=Q.to((u.liter)/(u.second)) #From Calculations for Water Pump speed and assume oy_flowrate is negligible for now
Q_stock_PACl = oy_flowrate_PACl
C_sys_PACl = 50*(u.mg/u.L) #user input desired concentration of PACl in the system

C_stock_PACl = (Q_sys*C_sys_PACl)/Q_stock_PACl
print('The PACl concentration in the stock is: ' +str(C_stock_PACl))
#M1V1=M2V2 to obtain volume of fluoride stock needed
M_superstock_PACl = (70.28 * (u.g/u.L)).to(u.mg/u.L) #concentration of fluoride provided
M_stock_PACl = C_stock_PACl
V_stock_PACl = 0.5 * u.L #total volume of the stock (water+fluoride)
V_superstock_PACl = (M_stock_PACl*V_stock_PACl)/M_superstock_PACl
print('The PACl superstock volume in the stock is: ' +str((V_superstock_PACl).to(u.milliliter)))
V_water_PACl = V_stock_PACl-V_superstock_PACl
print('The water volume in the PACl stock is : ' +str((V_water_PACl).to(u.milliliter)))



#USE THIS
import math as m
import numpy as np
from aguaclara.play import*

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

#PACl
#Concentration of PACl stock
C_stock_PACl = 1000*u.mg/u.L
#Concentration of PACl that you want in the reactor
C_reactor_PAC = 35*u.mg/u.L
#Flow rate of PACl in mL/s (put into ProCoDA)
Q_stock_PAC = Q_reactor*(C_reactor_PAC/C_stock_PACl)
print('PACl should be set in ProCoDA to: '+ str(Q_stock_PAC))

#RED DYE
#Concentration of red dye stock
#C_stock_dye = 1000*u.mg/u.L
#Concentration of dye that you want in the reactor
#C_reactor_dye = (Q_stock_PAC*C_stock_dye)/Q_reactor

#FLUORIDE
#Concentration of fluoride stock
C_stock_F = 1000*u.mg/u.L
#Concentration of fluoride that you want in the reactor
C_reactor_F = 5*u.mg/u.L
#Fluoride microtubing (orange-yellow)
oy_tube=0.019*u.mL/u.revolutions
#Flow rate of fluoride in mL/s (check in ProCoDA)
Q_stock_F = Q_reactor*(C_reactor_F/C_stock_F)
print('Fluoride can be set in ProCoDA to: '+str(Q_stock_F))
#Flow rate of fluoride in RPM (put into manual pump)
Q_stock_F_rpm = (Q_reactor/oy_tube)*(C_reactor_F/C_stock_F)*60*u.sec/u.min
print('Fluoride pump should be set at: '+str(Q_stock_F_rpm))

#WATER
#Flow rate of water in mL/s (put into ProCoDA)
Q_tap = Q_reactor - 1*Q_stock_PAC
print('Water should be set in ProCoDA to: '+str(Q_tap))
water_tube = 0.8*u.mL/u.s
Q_tap_rpm = (Q_reactor/(water_tube*u.mL))*(60*u.sec))
