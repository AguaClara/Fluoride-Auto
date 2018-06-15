```python
from aide_design.play import*
from aguaclara_research import tube_sizing as ts

Q_plant = 0.7601 * (u.mL/u.s)#flow rate of the plant
C = 5 * (u.mg/u.L)#desired concentration of the material within the plant
tubing_color = "orange-yellow"#color of the tubing to be used

stock = ts.C_stock_max(Q_plant, C, tubing_color)
print(stock)
```
