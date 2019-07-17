```python
import aguaclara.research.procoda_parser as pp
import scipy.stats as stats
import pandas as pd
import numpy as np
import scipy as sp
import scipy.optimize as opt
from aguaclara.play import *

flow_rates = pd.read_csv('/Users/melissalouie/Fluoride-Auto/Summer 2019/New Pump Flow Rates.csv')
expected_rate = flow_rates.iloc[:,0]
actual_rate = flow_rates.iloc[:,1]
rpm = flow_rates.iloc[:,2]

# ax1 is the axis handle for the first y-axis
fig, ax1 = plt.subplots()
ax1.set_xlabel("RPM")
ax1.set_ylabel("Expected Flow Rate (mL/s)")
# line1 is the line handle for the effluent_turbidity graph
expected_plot, = ax1.plot(rpm, expected_rate, color="blue")
linreg

ax2 = ax1.twinx()
ax2.set_ylabel("Actual Flow Rate (mL/s)")
actual_plot, = ax2.plot(rpm, actual_rate, color="red")

plt.title("Actual vs. Expected Flow Rates")
