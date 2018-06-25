# Fluoride, Summer 2018
#### Ching Pang, Kevin Sarmiento, Cheer Tsang
#### July 29, 2018

## Abstract
Briefly summarize your previous work, goals and objectives, what you have accomplished, and future work. (100 words max)

## Introduction
Explain how the completion of your challenge will affect AguaClara and the mission of providing safe drinking water (or sustainable wastewater treatment!). If this is a continuing team, how will your contribution build upon previous research? What needs to be further discovered or defined? If this is a new team, what prompted the inclusion of this team?

The recent expansion of AguaClara technology to new places around the world, like India, has uncovered new challenges and prompted new goals for AguaClara. In Honduras, where the majority of AguaClara plants have been constructed, the source of water designated for filtration comes from surface waters such as rivers and lakes. These waters typically have a high amount of particulate matter and as a result also carry biological contaminants. However, in India 85% of the population drinks groundwater extracted from wells. Contrast to surface water sources like in Honduras, groundwater contains nearly no particulate matter as many of the particles have been naturally filtered out as the water percolates through the soil and rock material. While this natural filtration process is capable of removing particulate matter it also offers the opportunity for minerals and metals to leach into the water. The kind of mineral and metal deposits depend heavily on the types of parent rock material and soils found in the region. India lies on what is known as one of the Fluoride Belts which are expanses of land that are geologically fluoride rich and have a much greater capacity to leach fluoride into the groundwater. According to the World Health Organization one of these belts stretches from Syria through Jordan, Egypt, Libya, Algeria, Sudan, and Kenya while another starts in Turkey and goes through Iraq, Iran, Afghanistan, India, Northern Thailand, and China (2016).

There are a number of public health implications associated with both underconsumption and overconsumption of fluoride. Fluoride is a common additive to municipal water systems in places like the United States where there is little to no fluoride naturally present in the water. Fluoride is added in order to prevent the onset of dental caries. New York City for example adds fluoride to its water supply in order to achieve a concentration of 0.7mg/L in their effluent supply (NYC DEP, 2016). 0.7mg/L is the agreed upon recommendation for fluoride by the American Dental Association for the prevention of dental cavities (ADA, 2017). There are however a number of health hazards associated with the consumption of fluoride at or over 1.5 mg/L in drinking water as set by the World Health Organization.




NYC DEP. (2016). New York City 2016 Drinking Water Supply and Quality Report. Retrieved from http://www.nyc.gov/html/dep/pdf/wsstate16.pdf

ADA. (2017). Fluoride: Topical and Systemic Supplements. Retrieved from https://www.ada.org/en/member-center/oral-health-topics/fluoride-topical-and-systemic-supplements

Water-related diseases. (2016). World Health Organization. Retrieved from http://www.who.int/water_sanitation_health/diseases-risks/diseases/fluorosis/en/

## Literature Review and Previous Work
Discuss what is already known about your research area based on both external work and that of past AguaClara Teams. Connect your objectives with what is already known and explain what additional contribution you intend to make. Make sure to add APA formatted in-text citations. If you mention the author(s) in your sentence, you can simply give the year of publication.[(Logan et. al. 1987)](http://www.jstor.org/stable/pdf/25043431.pdf?acceptTC=true)


## Methods

### Experimental Apparatus

The experimental apparatus included pumps, a coiled flocculator, and a sedimentation tube ([Figure 1](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Bench%20setup.png)). Water flows into the system through the water pump. Fluoride and coagulant (PACl) are pumped into the system from their respective stock tanks. The water, fluoride, and PACl mixture flows into the coiled flocculator. In the flocculator, PACl particles collide with fluoride ions, forming flocs. The mixture flows from the coiled flocculator to the sedimentation tube. Water flows up the sedimentation tube at a rate of 1.5 mm/s. This upflow velocity was used to calculate the necessary flow rate of water through the system. Calculations for the system flow rate can be found [here](https://github.com/AguaClara/fluoride/blob/master/SummerFluorideCalculations.md). Flocs are pumped from the sedimentation tube by a 1 rpm waste pump and exit through the floc weir. The treated water exits the sedimentation tube through the top where it flows to a sampling container. A sample is taken from the sampling container and the fluoride of the effluent water is measured by a fluoride probe.

![bench_setup](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Bench%20setup.png?raw=true)
Figure 1: The bench setup for the fluoride removal system.

Calculations for stock concentrations


* Design (calculations, constraints)

  $\frac{-b\pm\sqrt{b^2-4ac}}{2a}$
* Schematic (label parts)

  <img src="https://github.com/jillianwhiting/Jillian-Whiting/blob/master/Images/IMG_0009.jpg?raw=true" height=250 width=200>

* Image (from lab; label parts)
* Materials (dimensions, materials)
* Complications in construction
* If already constructed: write a brief summary of important constraints, include any revisions to apparatus, also reference the prior report where construction is described


### Procedure
Discuss your experimental procedure. How did you run your experiment? What were you testing? What were the values of relevant parameters?

## Results and Analysis
Present an observation (results), then explain what happened (analysis).  Each paragraph should focus on one aspect of your results. In that same paragraph, you should interpret that result.  
In other words, there should not be two distinct paragraphs, but instead one paragraph containing one result and the interpretation and analysis of this result. Here are some guiding questions for results and analysis:

When describing your results, present your data, using the guidelines below:
* What happened? What did you find?
* Show your experimental data in a professional way.
```python
from aide_design.play import*
x = np.array([1,2,3,4,5])
y = np.array([1,2,3,4,5])
plt.figure('ax',(10,8))
plt.plot(x,y,'*')
plt.savefig('/Users/jillianwhiting/github/Jillian-Whiting/Images/linear')
plt.show()
```
![linear](https://github.com/jillianwhiting/Jillian-Whiting/blob/master/Images/linear.png?raw=true)
Figure 1: Captions are very important for figures. Captions go below figures.

After describing a particular result, within a paragraph, go on to connect your work to fundamental physics/chemistry/statics/fluid mechanics, or whatever field is appropriate. Analyze your results and compare with theoretical expectations; or, if you have not yet done the experiments, describe your expectations based on established knowledge. Include implications of your results. How will your results influence the design of AguaClara plants? If possible provide clear recommendations for design changes that should be adopted. Show your experimental data in a professional way using the following guidelines:
* Why did you get those results/data?
* Did these results line up with expectations?
* What went wrong?
* If the data do not support your hypothesis, is there another hypothesis that describes your new data?

## Conclusions
Explain what you have learned and how that influences your next steps. Why does what you discovered matter to AguaClara?

Make sure that you defend your conclusions with facts and results.

## Future Work
Describe your plan of action for the next several weeks of research. Detail the next steps for this team. How can AguaClara use what you discovered for future projects? Your suggestions for challenges for future teams are most welcome. Should research in this area continue?

## Bibliography
Logan, B. E., Hermanowicz, S. W., & Parker,A. S. (1987). A Fundamental Model for Trickling Filter Process Design. Journal (Water Pollution Control Federation), 59(12), 1029–1042.

# Manual

## Fabrication Details
### Reactors
The reactor in both the bench system and the gravity powered system were poorly welded and have leakages. Therefore, two new reactors were fabricated by cutting out 2 sets of PVC pipes for the tube settler (90 cm) and floc weir (40 cm) according to [2017 Fall HRS team final report](https://confluence.cornell.edu/display/AGUACLARA/High+Rate+Sedimentation?preview=/327614520/350974719/high-rate-sedimentation%20(5).pdf).
Bent in reactor is created using welder at 60 degrees from horizontal. Drill bit of 1/2 inch and thread of 1/4 inch were used.
Drilled hole into reactor for floc weir using circle saw and drill press at 55 degree angle.
Started welding floc weir pipe to tube settler.

## Experimental Methods
### Set-up
Step 1.
* Put tasks in a sequential order.
* It is okay to have sub-lists.
  - Like this.

### Experiment
Step 1.

### Cleaning Procedure
Step 1.

## Experimental Checklist
Another potential section could include a list of things that you need to check before running an experiment.

## ProCoDA Method File
Use this section to explain your method file. This could be broken up into several components as shown below:

### States
Here, you should describe the function of each state in your method file, both in terms of its overall purpose and also in terms of the details that make it distinct from other states. For example:
\begin{itemize}
\item \underline{OFF} - Resting state of ProCoDA. All sensors, relays, and pumps are turned off.
\end{itemize}

### Set Points
Here, you should list the set points used in your method file and explain their use as well as how each was calculated.

## Python Code

### Variables
$g$: gravity
$\sigma$: dispersion
$a$: amplitude
$h$: water depth
$H$: distance from wave crest to trough (2$a$)
$T$: wave period
$\lambda$: wavelength
$k$: wavenumber
$c_p$: celerity (wave phase speed)
$P$: pressure
$F$: force
$u$, $w$: x-velocity, z-velocity components

```python
import math as m
import numpy as np
from aide_design.play import*
from aguaclara_research import tube_sizing as ts

D=(1)*u.inch
D=D.to(u.m)
A=np.pi*(D**2)/4
print(A)
v=(0.0015)*(u.m/u.s)
#Area given our diameter of tubing
Q=(A*v)
print(Q)
Q=Q.to((u.milliliter)/(u.second))
print(Q)
#Manual calculation of RPM
Man_RPM=(Q/((0.8)*(u.milliliter)))
Man_RPM=Man_RPM*(60*(u.second))
print(Man_RPM)

"""Calculates maximum stock concentration and flow rate of fluoride stock given desired concentration in the plant"""

Q_plant = 0.7601 * (u.mL/u.s)#flow rate of the plant
C_fluoride = 5 * (u.mg/u.L)#desired concentration of the material within the plant
tubing_color = "orange-yellow"#color of the tubing to be used

C_stock_max_fluoride = ts.C_stock_max(Q_plant, C_fluoride, tubing_color)
print('Maximum stock concentration of fluoride given desired concentration in the plant: '+str(C_stock_max_fluoride))

Q_stock_max_fluoride = ts.Q_stock_max(Q_plant, C_fluoride, tubing_color)
print('Flow rate of the stock of the desired concentration: '+ str(Q_stock_max_fluoride))


"""Calculates maximum stock concentration and flow rate of PACl stock given desired concentration in the plant"""

C_PACl = 6.25 * (u.mg/u.L)#desired concentration of the material within the plant

stock = ts.C_stock_max(Q_plant, C_PACl, tubing_color)
print('Maximum stock concentration of fluoride given desired concentration in the plant: '+str(stock))

stock_flowrate = ts.Q_stock_max(Q_plant, C_PACl, tubing_color)
print('Flow rate of the stock of the desired concentration: '+ str(stock_flowrate))

V_stock_PACl = 1 * u.L
C_super_stock_PACl = 70.28 * (u.g/u.L)

V_super_stock_PACl = ts.V_super_stock(Q_plant, C_PACl, tubing_color, V_stock_PACl, C_super_stock_PACl)
print('The volume of PACl super stock added to the stock container to reach the desired concentration within the plant: ' + str(V_super_stock_PACl))

V_stock_fluoride = 1 * u.L
time_experiment_f = ts.T_stock(Q_plant, C_fluoride, tubing_color, V_stock_fluoride)
print(time_experiment_f)

V_stock_PACl = 1 * u.L
time_experiment_PACl = ts.T_stock(Q_plant, C_PACl, tubing_color, V_stock_PACl)
print(time_experiment_PACl)


```

```python
# To convert the document from markdown to pdf
pandoc Name_of_this_file.md -o TeamName_Research_Report.pdf
```
