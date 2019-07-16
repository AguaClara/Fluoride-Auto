```python
import matplotlib.pyplot as plt
import aguaclara.research.procoda_parser as pp
import scipy.stats as stats
import pandas as pd
import numpy as np
import scipy as sp
import scipy.optimize as opt
from aguaclara.play import *

july10exp = "/Users/melissalouie/Fluoride-Auto/Summer 2019/Data and Graphs/7-10-19/datalog 7-10-2019.xls"
data_raw = pd.read_csv(july10exp, delimiter="\t")
data = pp.remove_notes(data_raw)
time = pd.to_numeric(data.iloc[:,4]/60)
fluoride = pd.to_numeric(data.iloc[:,2])
#fluoride_plot, = plt.plot(time, fluoride, "b-")
turbidity = pd.to_numeric(data.iloc[:,3])
#turbidity_plot, = plt.plot(time, turbidity, "m-")

# ax1 is the axis handle for the first y-axis
fig, ax1 = plt.subplots()
ax1.set_xlabel("Time (minutes)")
ax1.set_ylabel("Effluent Fluoride Concentration (mg/L)")
# line1 is the line handle for the effluent_turbidity graph
fluoride_plot, = ax1.plot(time, fluoride, color="blue")


# ax2 is an axis handle for the second y-axis, with the same x-axis as ax1
ax2 = ax1.twinx()
ax2.set_ylabel("Effluent Turbidity (NTU)")
ax2.set_ylim(0,5)
# line1 is the line handle for the effluent_turbidity graph
turbidity_plot, = ax2.plot(time, turbidity, color="green")

```
