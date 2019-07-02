```python
import matplotlib.pyplot as plt
import pandas as pd
import scipy.stats as stats
import numpy as np
import scipy.optimize as opt

#import working experiments
summer19 = pd.read_csv('')
summer19_effluent=summer19noclay.iloc[:,1]
summer19_uptake=summer19noclay.iloc[:,4]
summer19plot, =plt.plot(summer19_effluent,summer19_uptake,"mo")
