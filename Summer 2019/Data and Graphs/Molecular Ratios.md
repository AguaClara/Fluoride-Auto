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
np.polyfit(np.log(effluent_fluoride),ratio,1)
# line of best fit for data: uptake = 1.47516487 log(effluent) + 0.10178618

bestfit_effluent = np.array(np.linspace(0.45,12))
bestfit_uptake = 1.47516487 * np.log(bestfit_effluent) + 0.10178618
bestfit_plot, = plt.plot(bestfit_effluent, bestfit_uptake, "g")

plt.title("Uptakes of Fluoride Atoms by PACl Molecules")
plt.xlabel("Effluent Fluoride (mg/L)")
plt.ylabel("Uptake (Atoms Fluoride/Molecules PACl)")
plt.legend((bestfit_plot), ("Uptake equals 1.47516487timeslog(effluent) plus 0.10178618"))

plt.savefig("Uptakes of Fluoride Atoms by PACl Molecules")


```
