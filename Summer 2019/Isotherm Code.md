```python
import matplotlib.pyplot as plt
import pandas as pd
import scipy.stats as stats
import numpy as np
import scipy.optimize as opt

# import the summer 2018 data: summer18
summer18 = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Spring%202019/Langmuir%20Isotherm%20Data/Summer%202018%20data%20points.csv')
summer18_effluent=summer18.iloc[:,0]
summer18_uptake=summer18.iloc[:,1]
summer18plot, =plt.plot(summer18_effluent,summer18_uptake,"ro")

# import the fall 2018 data: fall18
fall18 = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Spring%202019/Langmuir%20Isotherm%20Data/Fall%202018%20data.csv')
fall18_effluent=fall18.iloc[:,0]
fall18_uptake=fall18.iloc[:,1]
fall18plot, =plt.plot(fall18_effluent,fall18_uptake,"bo")

# import the spring 2019 data: spring19
spring19 = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Spring%202019/Langmuir%20Isotherm%20Data/Spring%202019%20data.csv')
spring19_effluent=spring19.iloc[:,0]
spring19_uptake=spring19.iloc[:,1]
spring19plot, =plt.plot(spring19_effluent,spring19_uptake,"ys")

# import the summer 2019 data: summer19
summer19 = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Summer%202019/Summer%202019%20data.csv')
summer19_effluent=summer19.iloc[4,1]
summer19_uptake=summer19.iloc[4,3]
summer19plot, =plt.plot(summer19_effluent,summer19_uptake,"ms")

# find the logarithmic line of best fit for the data
alldata=pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Spring%202019/Langmuir%20Isotherm%20Data/All%20Experimental%20Data%20Points.csv')
alldata_effluent=alldata.iloc[:,0]
alldata_uptake=alldata.iloc[:,1]
alldata_theoretical_uptake=alldata.iloc[:,2]
np.polyfit(np.log(alldata_effluent),alldata_uptake,1)
# line of best fit for data: uptake = 95.63250099 log(effluent) + 131.89094095

# graph line of best fit with data points
bestfit_effluent = np.array(np.linspace(0.45,12))
bestfit_uptake =  95.63250099 * np.log(bestfit_effluent) + 131.89094095
bestfit_plot, =plt.plot(bestfit_effluent,bestfit_uptake)

# find r^2 value for line of best fit
log_alldata_effluent=np.log(np.array(alldata_effluent))
linreg = stats.linregress(log_alldata_effluent, alldata_uptake)
slope, intercept, r_value = linreg[0:3]
print("R-squared for line of best fit", (r_value ** 2))

# get theoretical Langmuir Isotherm
theoretical = pd.read_csv('https://raw.githubusercontent.com/AguaClara/Fluoride-Auto/master/Spring%202019/Langmuir%20Isotherm%20Data/theoretical%20data%20points.csv')
theoretical_effluent=theoretical.iloc[:,0]
theoretical_uptake=theoretical.iloc[:,1]
theoreticalplot, =plt.plot(theoretical_effluent,theoretical_uptake,"m")

# plot the data set
plt.xlim(0, 11)
plt.ylim(0,400)
plt.xlabel("Effluent Fluoride Concentration (mg/L)")
plt.ylabel("Uptake (mg Fluoride/g PaCl)")
plt.legend((summer18plot, fall18plot, spring19plot, summer19plot, bestfit_plot,theoreticalplot),("Summer 2018", "Fall 2018", "Spring 2019", "Line of Best Fit","Theoretical Langmuir Isotherm"))
