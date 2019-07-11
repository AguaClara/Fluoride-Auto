```python
import matplotlib.pyplot as plt
import aguaclara.research.procoda_parser as pp
import scipy.stats as stats
import pandas as pd
import numpy as np
import scipy as sp
import scipy.optimize as opt
from aguaclara.play import *

july10exp = "https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/7-10-19/datalog%207-10-2019%20updated.xls"
data_raw = pd.read_csv(july10exp, delimiter=" ")
data = pp.remove_notes(data_raw)
time = data.iloc[:,0]
time_number = pd.to_numeric(time)
fluoride = data.iloc[:,3]
turbidity = data.iloc[:,2]

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
