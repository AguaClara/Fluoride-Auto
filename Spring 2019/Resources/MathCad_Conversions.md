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

#PACl
#Concentration of PACl stock
C_stock_PACl = 1000*u.mg/u.L
#Concentration of PACl that you want in the reactor
C_reactor_PAC = 30*u.mg/u.L
#Flow rate of PACl in mL/s (put into ProCoDA)
Q_stock_PAC = Q_reactor*(C_reactor_PAC/C_stock_PACl)

#RED DYE
#Concentration of red dye stock
C_stock_dye = 1000*u.mg/u.L
#Concentration of dye that you want in the reactor
C_reactor_dye = (Q_stock_PAC*C_stock_dye)/Q_reactor

#FLUORIDE
#Concentration of fluoride stock
C_stock_F = 1000*u.mg/u.L
#Concentration of fluoride that you want in the reactor
C_reactor_F = 5*u.mg/u.L
#Fluoride microtubing (orange-yellow)
oy_tube=0.019*u.mL/u.revolutions
#CHECK THIS WITH PROCODA TMW, NOT SURE IF IT IS correct:
#Flow rate of fluoride in RPM (put into manual pump)
Q_stock_F = (Q_reactor/oy_tube)*(C_reactor_F/C_stock_F)*60*u.sec/u.min
print ('Fluoride pump should be set at: ')
print(Q_stock_F)

#WATER
#Flow rate of water in mL/s (put into ProCoDA)
Q_tap = Q_reactor - 1*Q_stock_PAC

#Not sure if this is correct right now: Q_fluoride = (0.5)*Q_tap

#Fix this part of the code --> not sure what it's for because it has fluoride and dye included
#Flow rate of fluoride in mL/s (put into ProCoDA)
#Q_fluoride = (Q_reactor * C_reactor_F)/(C_stock_dye)

#C_stock_F = Q_reactor*(C_reactor_F/Q_fluoride)

#C_lab_PAC = 70900


#Flocculator Calculations

#Inputs
# flow rate in flocculator
Q_flocculator = Q_reactor.to(u.m**3/u.s)
# target G*theta to design the flocculator
Gtheta_goal = 20000
#inner diameter of the flocculator tubing
D_floctube = (0.125 * u.inch).to(u.meter)
#radius of curvature (the radius of the tube the flocculator is wrapped around)
R_c = (4.25 * u.cm).to(u.m)
# flocculator tubing length
L_flocculator = (46*u.ft).to(u.m)

#Reynolds number things
Re_pipetransition = 2100
v=1*10**-6 * u.m**2/u.s
e_PVC = (0.12 * u.mm).to(u.m)
Re_QDv = 4*Q_flocculator/m.pi/D_floctube/v

# friction factor
if Re_QDv > Re_pipetransition
  f=0.25/(m.log10(e_PVC/(3.7*D_floctube)+5.74/(Re_QDv)**0.9))**2
  print(f)
else:
  f=64/Re_QDv
  print(f)

# headloss
g=(9.81*u.m/u.s**2)
h_f = f*8*L_flocculator*Q_flocculator**2/g/m.pi**2/D_floctube**5

De = m.sqrt(D_floctube/R_c)*Re_QDv
friction_ratio=1+0.033*m.log(De)**4
h_friction = h_f*friction_ratio

# Cross-sectional area of floctube piping
Area_floctube=m.pi/4*D_floctube**2

# ED and e_floc (?)
ED_flocculator = h_friction*g/theta
e_floc = (ED_flocculator).to(u.mW/u.kg)

#G_floc (?)
G_floc = m.sqrt((e_floc/v).to(u.s**-2)*u.s**2)*u.s**-1
print(G_floc)

# theta goal
theta_goal=Gtheta_goal/G_floc

# L floc
L_floc=theta_goal*Q_flocculator/Area_floctube

# Residence time of design Flocculator
theta_flocculator = Area_floctube*L_flocculator/Q_flocculator

#Gtheta of design Flocculator
G_floc*theta_flocculator

#Calculating gamma from fractal floc model
#Percent of flow going to flocs and water
ratio_water = 0.8
ratio_flocs = 1-ratio_water
#Raw water pump flow ratio_water
Q_water = ratio_water * Q_reactor
#Total flocs pump flow rate
Q_floc = ratio_flocs * Q_reactor
#Flow rate of PACl pump head
Q_PACl = Q_floc/2
#Flow rate of dye pump head
Q_dye = Q_floc/2

H_fb = 24 * u.inch
#Should be between 2000 and 6000 mg/L
C_fb_clay = 100 * u.mg/u.L
V_fb = V_up * (C_reactor_dye/C_fb_clay)
#Time for the floc blanket to form
T_fb = H_fb/V_fb

#Concentration of PACl we want in the stock tank
C_PACl_desired = 250 * u.mg/u.L
#Current volume in stock tank
V_stockPACl_now = 10 * u.L
#Mass of PACl we need in the stock tank
M_PACl_desired = C_PACl_desired * V_stockPACl_now
#Current concentration of PACl in stock tank
C_stockPACl_now = 0 * u.mg/u.L
#Current mass of PACl in stock tank
M_PAClstock_now = C_stockPACl_now * V_stockPACl_now
#Mass of PACl that we need to add to the stock tank
M_PACl_needed = M_PACl_desired - M_PAClstock_now

#Volume of lab PACl that we need to add to the stock tank
V_PACl_needed = M_PACl_needed/C_lab_PAC

#Time to refill the stock tanks
#Measure to liter bar above the output

Q_coagulantflow = Q_stock_PAC
V_liters_left = 21 * u.L
T_refill = V_liters_left/Q_coagulantflow
T_refill_F = V_liters_left/Q_fluoride

C_fluoride_stock = 1000 * u.mg/u.L
V_fluoride_sample = 100 * u.mL
C_fluoride_sample = 20 * u.mg/u.L

C_clay_stock = 1200 * u.mg/u.L
C_new_stock = 1000 * u.mg/u.L
V_clay_stock = 0.17 * u.L
V_new_clay = C_clay_stock * (V_clay_stock/C_new_stock)

#1 is set as the flocculator length. L cancels in the calculation.
