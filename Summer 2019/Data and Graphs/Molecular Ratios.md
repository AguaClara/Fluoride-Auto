```python
import matplotlib.pyplot as plt
import pandas as pd
import scipy.stats as stats
import numpy as np
import scipy.optimize as opt

data = pd.read_csv("https://github.com/AguaClara/Fluoride-Auto/blob/master/Summer%202019/Data%20and%20Graphs/Molecular%20Ratios.csv?raw=true")
effluent_fluoride = pd.to_numeric(data.iloc[:,4])
ratio = pd.to_numeric(data.iloc[:,8])

fluoride_plot, = plt.plot(effluent_fluoride, ratio, "mo")
plt.title("Uptakes of Fluoride Atoms by PACl Molecules")
plt.xlabel("Effluent Fluoride (mg/L)")
plt.ylabel("Uptake (Atoms Fluoride/Molecules PACl)")
plt.savefig("Uptakes of Fluoride Atoms by PACl Molecules")



```
