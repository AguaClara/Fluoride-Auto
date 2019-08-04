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
summer19_grav_effluent=pd.to_numeric(summer19grav.iloc[:,2])
summer19_grav_uptake=pd.to_numeric(summer19grav.iloc[:,5])
summer19gravplot, =plt.plot(summer19_grav_effluent, summer19_grav_uptake,"cs")

alldata=pd.read_csv("https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/Summer%202019%20Working%20Data.csv")
alldata_effluent=alldata.iloc[:,2]
alldata_uptake=alldata.iloc[:,5]
np.polyfit(np.log(alldata_effluent),alldata_uptake,1)
# line of best fit for data: uptake = 132.63782551 log(effluent) + 9.16487889

bestfit_effluent = np.array(np.linspace(0.45,12))
bestfit_uptake =  132.63782551 * np.log(bestfit_effluent) + 9.16487889
bestfit_plot, =plt.plot(bestfit_effluent,bestfit_uptake)

theoretical = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Spring%202019/Langmuir%20Isotherm%20Data/theoretical%20data%20points.csv')
theoretical_effluent=theoretical.iloc[:,0]
theoretical_uptake=theoretical.iloc[:,1]
theoreticalplot, =plt.plot(theoretical_effluent,theoretical_uptake,"m")

plt.title("Summer 2019 Uptake vs. Effluent Successful Experiments")
plt.xlim(0,15)
plt.ylim(0,400)
plt.xlabel("Effluent Fluoride Concentration (mg/L)")
plt.ylabel("Uptake (mg Fluoride/g PaCl)")
plt.legend((summer19autoplot, summer19gravplot, bestfit_plot, theoreticalplot), ("Automated System", "Gravity System", "Summer 2019 Line of Best Fit", "Isotherm Used in Previous Semesters"))
plt.savefig("Working Graphs")
```
