```python
import matplotlib.pyplot as plt
import aguaclara.research.procoda_parser as pp
import scipy.stats as stats
import pandas as pd
import numpy as np
import scipy as sp
import scipy.optimize as opt
from aguaclara.play import *

#Plot floc blanket height vs. time
flocdata = "https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/7-12-19/Floc%20Blanket%20712.csv"
floc_raw = pd.read_csv(flocdata, delimiter="\t")
time = floc_raw.iloc[:,1]
height = floc_raw.iloc[:,2]
plt.plot(time, height)
plt.xlim(0,4000)
plt.ylim(0,65)
plt.title("Height of the Floc Blanket over Time")
plt.xlabel("Time (sec)")
plt.ylabel("Height from Bottom of Sedimentation Tube (cm)")
plt.savefig("Floc Blanket Graph 7-12")

```
