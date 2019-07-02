```python
import matplotlib.pyplot as plt
import pandas as pd
import scipy.stats as stats
import numpy as np
import scipy.optimize as opt

# import the summer 2019 data without clay: summer19noclay
summer19noclay = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/No%20Clay.csv')
summer19_noclay_effluent=summer19noclay.iloc[:,1]
summer19_noclay_uptake=summer19noclay.iloc[:,4]
summer19noclayplot, =plt.plot(summer19_noclay_effluent,summer19_noclay_uptake,"mo")

# import the summer 2019 data with clay: summer19clay
summer19clay = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Clay.csv')
summer19_clay_effluent=summer19clay.iloc[:,1]
summer19_clay_uptake=summer19clay.iloc[:,4]
summer19clayplot, =plt.plot(summer19_clay_effluent,summer19_clay_uptake,"bo")

# plot the data set
plt.title("Summer 2019 Uptake vs. Effluent Points")
plt.xlim(0,6)
plt.ylim(0,200)
plt.xlabel("Effluent Fluoride Concentration (mg/L)")
plt.ylabel("Uptake (mg Fluoride/g PaCl)")
plt.legend((summer19noclayplot, summer19clayplot),("No Clay", "Clay"))
plt.savefig("Summer 2019 Graph")
