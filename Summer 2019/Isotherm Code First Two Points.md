```python
import matplotlib.pyplot as plt
import pandas as pd
import scipy.stats as stats
import numpy as np
import scipy.optimize as opt

# import the summer 2019 data: summer19
summer19 = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Summer%202019%20data.csv')
summer19_effluent=summer19.iloc[:,1]
summer19_uptake=summer19.iloc[:,3]
summer19plot, =plt.plot(summer19_effluent,summer19_uptake,"ms")

# plot the data set
plt.xlim(0, 11)
plt.ylim(0,100)
plt.xlabel("Effluent Fluoride Concentration (mg/L)")
plt.ylabel("Uptake (mg Fluoride/g PaCl)")
plt.legend((summer19plot), ('Summer 2019'))
