```python
import aguaclara.research.procoda_parser as pp
import scipy.stats as stats
import pandas as pd
import numpy as np
import scipy as sp
import scipy.optimize as opt
from aguaclara.play import *

july12exp = "https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/7-12-19/datalog%207-12-2019.xls"
data_raw = pd.read_csv(july12exp, delimiter="\t")
data = pp.remove_notes(data_raw)
time = pd.to_numeric(data.iloc[:,5])/60
fluoride = data.iloc[:,2]
turbidity = data.iloc[:,4]
floc_blanket = data.iloc[:,6]

#Graph fluoride concentration and turbidity vs. time
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
ax2.set_ylim(0,1)
# line1 is the line handle for the effluent_turbidity graph
turbidity_plot, = ax2.plot(time, turbidity, color="green")

plt.title("7-12-19 Effluent Fluoride Concentration and Turbidity")
plt.legend((fluoride_plot, turbidity_plot),("Fluoride Concentration","Turbidity"))
plt.savefig("7-12-19 Effluent Fluoride Concentration and Turbidity")



#Graph fluoride concentration and floc blanket height vs. time
# ax1 is the axis handle for the first y-axis
fig, ax3 = plt.subplots()
ax3.set_xlabel("Time (minutes)")
ax3.set_ylabel("Effluent Fluoride Concentration (mg/L)")
ax3.set_ylim(0,4)
# line1 is the line handle for the effluent_turbidity graph
fluoride_plot, = ax3.plot(time, fluoride, color="blue")

# ax2 is an axis handle for the second y-axis, with the same x-axis as ax1
ax4 = ax3.twinx()
ax4.set_ylabel("Floc Blanket Height (cm)")
ax4.set_ylim(0,90)
# line1 is the line handle for the effluent_turbidity graph
flocblanket_plot, = ax4.plot(time, floc_blanket, "ro")

plt.title("7-10-19 Floc Blanket Height and Fluoride Concentration over Time")
plt.legend((fluoride_plot, flocblanket_plot),("Fluoride Concentration (mg/L)","Floc Blanket Height (cm)"))
plt.savefig("7-10-19 Floc Blanket Height and Fluoride Concentration")



#Graph turbidity and floc blanket height vs. time
fig, ax5 = plt.subplots()
ax5.set_xlabel("Time (minutes)")
ax5.set_ylabel("Effluent Turbidity (NTU)")
ax5.set_ylim(0,4)
# line1 is the line handle for the effluent_turbidity graph
turbidity_plot, = ax5.plot(time, turbidity, color="green")

ax6 = ax5.twinx()
ax6.set_ylabel("Floc Blanket Height (cm)")
ax6.set_ylim(0,90)
# line1 is the line handle for the effluent_turbidity graph
flocblanket_plot, = ax6.plot(time, floc_blanket, "ro")

plt.title("7-12-19 Floc Blanket Height and Turbidity over Time")
plt.legend((fluoride_plot, flocblanket_plot),("Turbidity (NTU)","Floc Blanket Height (cm)"))
plt.savefig("7-12-19 Turbidity and Floc Blanket Height")

```
