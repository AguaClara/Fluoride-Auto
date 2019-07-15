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
fig, fluoride = plt.subplots()
fluoride.set_xlabel("Time (minutes)")
fluoride.set_ylabel("Effluent Fluoride Concentration (mg/L)")
# line1 is the line handle for the effluent_turbidity graph
fluoride_plot, = fluoride.plot(time, fluoride, color="blue")

# ax2 is an axis handle for the second y-axis, with the same x-axis as ax1
turbidity = fluoride.twinx()
turbidity.set_ylabel("Effluent Turbidity (NTU)")
turbidity.set_ylim(0,5)
# line1 is the line handle for the effluent_turbidity graph
line2, = turbidity.plot(time, turbidity, color="green")

#Plot floc blanket height vs. time
flocdata = "https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/7-10-19/Floc%20Blanket.csv"
floc_raw = pd.read_csv(flocdata)
time = floc_raw.iloc[:,1]
height = floc_raw.iloc[:,2]
plt.plot(time, height)
plt.xlim(0,1000)
plt.ylim(0,150)
plt.title("Height of the Floc Blanket over Time")
plt.xlabel("Time (sec)")
plt.ylabel("Height from Bottom of Sedimentation Tube (cm)")


```
