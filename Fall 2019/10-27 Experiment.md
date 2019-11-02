```python
import aguaclara.research.procoda_parser as pp
import scipy.stats as stats
import pandas as pd
import numpy as np
import scipy as sp
import scipy.optimize as opt
from aguaclara.play import *

#Import the datalog
turbidityexp = "https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Fall%202019/datalog%2010-27-2019.tsv"

#Read the data and remove textlog notes
data_raw = pd.read_csv(turbidityexp, delimiter="\t")
data = pp.remove_notes(data_raw)
time = pd.to_numeric(data.iloc[0:1112,1])/60
turbidity = data.iloc[0:1112,3]

time=data.iloc[6989:8044,0]
turbidity=data.iloc[6989:8044,4]
graph,=plt.plot(time, turbidity,"ro")
#graph.xlabel=("Time(seconds)")
#graph.ylabel=("Effluent Turbidity (NTU)")




# ax1 is the axis handle for the first y-axis
fig, ax1 = plt.subplots()
ax1.set_xlabel("Time (minutes)")
ax1.set_ylabel("Effluent Fluoride Concentration (mg/L)")
ax1.set_ylim(0,10)
# line1 is the line handle for the effluent_turbidity graph
fluoride_plot, = ax1.plot(time, fluoride, color="blue")
