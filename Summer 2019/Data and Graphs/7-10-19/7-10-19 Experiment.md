```python
import aguaclara.research.procoda_parser as pp
import scipy.stats as stats
import pandas as pd
import numpy as np
import scipy as sp
import scipy.optimize as opt
from aguaclara.play import *

july10exp = "https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Data%20and%20Graphs/datalog%207-9-2019%20w%20fluoride%20concentration.xls"
data_raw = pd.read_csv(july10exp)
data = pp.remove_notes(data_raw)
time = data.iloc[:,0]
time_number = pd.to_numeric(time)
fluoride = data.iloc[:,13]
turbidity = data.iloc[:,7]

#Plot floc blanket height vs. time
flocdata = ""

```
