```python
import matplotlib.pyplot as plt
import pandas as pd
import scipy.stats as stats
import numpy as np
import scipy.optimize as opt

#import working experiments
summer19 = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Working%20Experiments.csv')
summer19_effluent=summer19.iloc[:,1]
summer19_uptake=summer19.iloc[:,4]
summer19plot, =plt.plot(summer19_effluent,summer19_uptake,"mo")

plt.title("Summer 2019 Uptake vs. Effluent Working Experiments")
plt.xlim(0,6)
plt.ylim(0,175)
plt.xlabel("Effluent Fluoride Concentration (mg/L)")
plt.ylabel("Uptake (mg Fluoride/g PaCl)")
