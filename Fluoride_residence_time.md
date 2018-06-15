```python
from aide_design.play import*
from aguaclara_research import tube_sizing as ts

"""Calculates maximum stock concentration and flow rate of fluoride stock given desired concentration in the plant"""

Q_plant = 0.7601 * (u.mL/u.s)#flow rate of the plant
C = 5 * (u.mg/u.L)#desired concentration of the material within the plant
tubing_color = "orange-yellow"#color of the tubing to be used

stock = ts.C_stock_max(Q_plant, C, tubing_color)
print('Maximum stock concentration of fluoride given desired concentration in the plant: '+str(stock))

stock_flowrate = ts.Q_stock_max(Q_plant, C, tubing_color)
print('Flow rate of the stock of the desired concentration: '+ str(stock_flowrate))


"""Calculates maximum stock concentration and flow rate of PACl stock given desired concentration in the plant"""

Q_plant = 0.7601 * (u.mL/u.s)#flow rate of the plant
C = 6.25 * (u.mg/u.L)#desired concentration of the material within the plant
tubing_color = "orange-yellow"#color of the tubing to be used

stock = ts.C_stock_max(Q_plant, C, tubing_color)
print('Maximum stock concentration of fluoride given desired concentration in the plant: '+str(stock))

stock_flowrate = ts.Q_stock_max(Q_plant, C, tubing_color)
print('Flow rate of the stock of the desired concentration: '+ str(stock_flowrate))

V_stock = 1 * u.L
C_super_stock = 70.28 * (u.g/u.L)

PACl_V_super_stock = ts.V_super_stock(Q_plant, C, tubing_color, V_stock, C_super_stock)
print('The volume of PACl super stock added to the stock container to reach the desired concentration within the plant: ' + str(PACl_V_super_stock))


```
