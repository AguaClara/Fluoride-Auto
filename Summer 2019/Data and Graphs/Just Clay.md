```python
import matplotlib.pyplot as plt
import pandas as pd
import scipy.stats as stats
import numpy as np
import scipy.optimize as opt

# import the summer 2019 data with clay: summer19clay
summer19clay = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/Clay.csv')
summer19_clay_effluent=summer19clay.iloc[:,1]
summer19_clay_uptake=summer19clay.iloc[:,4]
summer19clayplot, =plt.plot(summer19_clay_effluent,summer19_clay_uptake,"bo")

# import the summer 2019 data without clay: summer19noclay
summer19noclay = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/No%20Clay.csv')
effluent1=summer19noclay.iloc[6,1]
effluent2=summer19noclay.iloc[14,1]
effluent3=summer19noclay.iloc[15,1]
uptake1=summer19noclay.iloc[6,4]
uptake2=summer19noclay.iloc[14,1]
uptake3=summer19noclay.iloc[15,1]
noclay1, = plt.plot(effluent1,uptake1, "go")
noclay2, = plt.plot(effluent2,uptake2, "go")
noclay3, = plt.plot(effluent3,uptake3, "go")

plt.title("Clay vs. No Clay Experiments")
plt.xlabel("Effluent Fluoride Concentration (mg/L)")
plt.ylabel("Uptake (mg Fluoride Removed / g PACl)")
plt.legend((summer19clayplot,noclay1),("Clay Experiments","No-Clay Experiments"))

```
