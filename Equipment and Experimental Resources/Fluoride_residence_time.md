```python
from aide_design.play import*
from aguaclara_research import tube_sizing as ts

"""Calculates maximum stock concentration and flow rate of fluoride stock given desired concentration in the plant"""

Q_plant = 0.7601 * (u.mL/u.s)#flow rate of the plant
C_fluoride = 3 * (u.mg/u.L)#desired concentration of the material within the plant
tubing_color = "orange-yellow" #color of the tubing to be used

C_stock_max_fluoride = ts.C_stock_max(Q_plant, C_fluoride, tubing_color)
print('Maximum stock concentration of fluoride given desired concentration in the plant: '+str(C_stock_max_fluoride))

Q_stock_max_fluoride = ts.Q_stock_max(Q_plant, C_fluoride, tubing_color)
print('Flow rate of the fluoride stock of the desired concentration: '+ str(Q_stock_max_fluoride))


"""Calculates maximum stock concentration and flow rate of PACl stock given desired concentration in the plant"""

C_PACl = 6.25 * (u.mg/u.L)#desired concentration of the material within the plant

stock = ts.C_stock_max(Q_plant, C_PACl, tubing_color)
print('Maximum stock concentration of fluoride given desired concentration in the plant: '+str(stock))

stock_flowrate = ts.Q_stock_max(Q_plant, C_PACl, tubing_color)
print('Flow rate of the PACl stock of the desired concentration: '+ str(stock_flowrate))

V_stock_PACl = 1 * u.L
C_super_stock_PACl = 70.28 * (u.g/u.L)

V_super_stock_PACl = ts.V_super_stock(Q_plant, C_PACl, tubing_color, V_stock_PACl, C_super_stock_PACl)
print('The volume of PACl super stock added to the stock container to reach the desired concentration within the plant: ' + str(V_super_stock_PACl))

V_stock_fluoride = 1 * u.L
time_experiment_f = ts.T_stock(Q_plant, C_fluoride, tubing_color, V_stock_fluoride)
print(time_experiment_f)

V_stock_PACl = 1 * u.L
time_experiment_PACl = ts.T_stock(Q_plant, C_PACl, tubing_color, V_stock_PACl)
print(time_experiment_PACl)


```
