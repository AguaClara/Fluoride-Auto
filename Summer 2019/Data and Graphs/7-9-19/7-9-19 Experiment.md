```python
import aguaclara.research.procoda_parser as pp
import scipy.stats as stats
import pandas as pd
import numpy as np
import scipy as sp
import scipy.optimize as opt
from aguaclara.play import *

july9exp = "https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/7-9-19/datalog%207-9-2019%20.xls"
data_raw = pd.read_csv(july9exp, delimiter="\t")
data = pp.remove_notes(data_raw)
time = data.iloc[:,1]/60
time_number = pd.to_numeric(time)
fluoride = data.iloc[:,3]
turbidity = data.iloc[:,5]

# ax1 is the axis handle for the first y-axis
fig, ax1 = plt.subplots()
ax1.set_xlabel("Time (minutes)")
ax1.set_ylabel("Effluent Fluoride Concentration (mg/L)")
ax1.set_ylim(0,2)
# line1 is the line handle for the effluent_turbidity graph
fluoride_plot, = ax1.plot(time, fluoride, color="blue")

# ax2 is an axis handle for the second y-axis, with the same x-axis as ax1
ax2 = ax1.twinx()
ax2.set_ylabel("Effluent Turbidity (NTU)")
ax2.set_ylim(0,5)
# line1 is the line handle for the effluent_turbidity graph
turbidity_plot, = ax2.plot(time, turbidity, color="green")
plt.title("7-9-19 Effluent Fluoride Concentration and Turbidity")
plt.legend((fluoride_plot, turbidity_plot),("Fluoride Concentration","Turbidity"))

plt.savefig("7-9-19 Effluent Fluoride Concentration and Turbidity")
