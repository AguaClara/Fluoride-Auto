```python
import aguaclara.research.procoda_parser as pp
import scipy.stats as stats
import pandas as pd
import numpy as np
import scipy as sp
import scipy.optimize as opt
from aguaclara.play import *

#Experiment 1
exp1 = "https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/7-15-19/7-15-19%20Experiment%201.csv"
data_raw = pd.read_csv(exp1, delimiter="\t")
data = pp.remove_notes(data_raw)
time = pd.to_numeric(data.iloc[:,5])/60
fluoride = data.iloc[:,2]
turbidity = data.iloc[:,4]

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
plt.title("7-15-19 Experiment 1")
plt.legend((fluoride_plot, turbidity_plot),("Fluoride Concentration","Turbidity"))

plt.savefig("7-15-19 Experiment 1")


#Experiment 2
exp2 = "https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/7-15-19/7-15-19%20Experiment%202.csv"
data_raw = pd.read_csv(exp2, delimiter="\t")
data = pp.remove_notes(data_raw)
time = pd.to_numeric(data.iloc[:,5])/60
fluoride = data.iloc[:,2]
turbidity = data.iloc[:,4]

# ax1 is the axis handle for the first y-axis
fig, ax3 = plt.subplots()
ax3.set_xlabel("Time (minutes)")
ax3.set_ylabel("Effluent Fluoride Concentration (mg/L)")
ax3.set_ylim(0,2)
# line1 is the line handle for the effluent_turbidity graph
fluoride_plot, = ax3.plot(time, fluoride, color="blue")

# ax2 is an axis handle for the second y-axis, with the same x-axis as ax1
ax4 = ax3.twinx()
ax4.set_ylabel("Effluent Turbidity (NTU)")
ax4.set_ylim(0,1)
# line1 is the line handle for the effluent_turbidity graph
turbidity_plot, = ax4.plot(time, turbidity, color="green")
plt.title("7-15-19 Experiment 2")
plt.legend((fluoride_plot, turbidity_plot),("Fluoride Concentration","Turbidity"))

plt.savefig("7-15-19 Experiment 2")


#Experiment 3
exp3 = "https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/7-15-19/7-15-19%20Experiment%203.csv"
data_raw = pd.read_csv(exp3, delimiter="\t")
data = pp.remove_notes(data_raw)
time = pd.to_numeric(data.iloc[:,5])/60
fluoride = data.iloc[:,2]
turbidity = data.iloc[:,4]

# ax1 is the axis handle for the first y-axis
fig, ax5 = plt.subplots()
ax5.set_xlabel("Time (minutes)")
ax5.set_ylabel("Effluent Fluoride Concentration (mg/L)")
ax5.set_ylim(0,2)
# line1 is the line handle for the effluent_turbidity graph
fluoride_plot, = ax5.plot(time, fluoride, color="blue")

# ax2 is an axis handle for the second y-axis, with the same x-axis as ax1
ax6 = ax5.twinx()
ax6.set_ylabel("Effluent Turbidity (NTU)")
ax6.set_ylim(0,1)
# line1 is the line handle for the effluent_turbidity graph
turbidity_plot, = ax6.plot(time, turbidity, color="green")
plt.title("7-15-19 Experiment 3")
plt.legend((fluoride_plot, turbidity_plot),("Fluoride Concentration","Turbidity"))

plt.savefig("7-15-19 Experiment 3")


#Experiment 4
exp4 = "https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/7-15-19/7-15-19%20Experiment%204.csv"
data_raw = pd.read_csv(exp4, delimiter="\t")
data = pp.remove_notes(data_raw)
time = pd.to_numeric(data.iloc[:,5])/60
fluoride = data.iloc[:,2]
turbidity = data.iloc[:,4]

# ax1 is the axis handle for the first y-axis
fig, ax7 = plt.subplots()
ax7.set_xlabel("Time (minutes)")
ax7.set_ylabel("Effluent Fluoride Concentration (mg/L)")
ax7.set_ylim(0,2)
# line1 is the line handle for the effluent_turbidity graph
fluoride_plot, = ax7.plot(time, fluoride, color="blue")

# ax2 is an axis handle for the second y-axis, with the same x-axis as ax1
ax8 = ax7.twinx()
ax8.set_ylabel("Effluent Turbidity (NTU)")
ax8.set_ylim(0,1)
# line1 is the line handle for the effluent_turbidity graph
turbidity_plot, = ax8.plot(time, turbidity, color="green")
plt.title("7-15-19 Experiment 4")
plt.legend((fluoride_plot, turbidity_plot),("Fluoride Concentration","Turbidity"))

plt.savefig("7-15-19 Experiment 4")

```
