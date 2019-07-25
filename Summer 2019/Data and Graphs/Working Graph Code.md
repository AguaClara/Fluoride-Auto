```python
import matplotlib.pyplot as plt
import pandas as pd
import scipy.stats as stats
import numpy as np
import scipy.optimize as opt

# import auto data
summer19auto = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/Working%20Experiments%20Auto.csv')
summer19_auto_effluent=summer19auto.iloc[:,2]
summer19_auto_uptake=summer19auto.iloc[:,5]
summer19autoplot, =plt.plot(summer19_auto_effluent,summer19_auto_uptake,"rs")

# import grav data
summer19grav = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/Working%20Experiments%20Grav.csv')
summer19_grav_effluent=summer19grav.iloc[:,2]
summer19_grav_uptake=summer19grav.iloc[:,5]
summer19gravplot, =plt.plot(summer19_grav_effluent, summer19_grav_uptake,"cs")

plt.title("Summer 2019 Uptake vs. Effluent Successful Experiments")
plt.xlim(0,20)
plt.ylim(0,400)
plt.xlabel("Effluent Fluoride Concentration (mg/L)")
plt.ylabel("Uptake (mg Fluoride/g PaCl)")
plt.legend((summer19autoplot, summer19gravplot), ("Automated System", "Gravity System"))
#plt.savefig("Working Graphs")
