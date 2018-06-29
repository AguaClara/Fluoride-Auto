# Fluoride, Summer 2018
#### Ching Pang, Kevin Sarmiento, Cheer Tsang
#### July 29, 2018

## Abstract
Briefly summarize your previous work, goals and objectives, what you have accomplished, and future work. (100 words max)

## Introduction

The recent expansion of AguaClara technology to new places around the world, like India, has uncovered new challenges and prompted new goals for AguaClara. In Honduras, where the majority of AguaClara plants have been constructed, the source of water designated for filtration comes from surface waters such as rivers and lakes. These waters typically have a high amount of particulate matter and as a result also carry biological contaminants. However, in India 85% of the population drinks groundwater extracted from wells and aquifers. Contrast to surface water sources like in Honduras, groundwater contains nearly no particulate matter as many of the particles are naturally filtered out as the water percolates through the soil and rock material. While this natural filtration process is capable of removing particulate matter and reducing microorganisms it also offers the opportunity for minerals and metals to leach into the water. The kinds of minerals that get into the water depend heavily on the types of parent rock material and soils found in the region. India lies on what is known as one of the Fluoride Belts which are expanses of land that are geologically fluoride rich and have a much greater capacity to leach fluoride into the groundwater. According to the World Health Organization one of these belts stretches from Syria through Jordan, Egypt, Libya, Algeria, Sudan, and Kenya while another starts in Turkey and goes through Iraq, Iran, Afghanistan, India, Northern Thailand, and China [(Water-related diseases, 2016)](http://www.who.int/water_sanitation_health/diseases-risks/diseases/fluorosis/en/). India contains about 14% of the total fluoride on the earth's crust, which inevitable leads some of it to leach into the groundwater [(Mondal, Dutta, & Gupta, 2016)](https://doi.org/10.1007/s10653-015-9743-7).

There are a number of public health implications associated with both underconsumption and overconsumption of fluoride. Fluoride is a common additive to municipal water systems in places like the United States where there is little to no fluoride naturally present in the water. Fluoride is added in order to prevent the onset of dental caries. New York City for example adds fluoride to its water supply in order to achieve a concentration of 0.7$\mathrm{\frac{mg}{L}}$ in their effluent supply [(NYC DEP, 2016)](http://www.nyc.gov/html/dep/pdf/wsstate16.pdf). The American Dental Association has set the recommended concentration of fluoride in drinking water at 0.7$\mathrm{\frac{mg}{L}}$ for the prevention of dental cavities [(ADA, 2017)](https://www.ada.org/en/member-center/oral-health-topics/fluoride-topical-and-systemic-supplements). There are however a number of health risks associated with the consumption of fluoride at higher concentrations.

The World Health Organization has set an absolute limit on the concentration of fluoride in drinking water at 1.5$\mathrm{\frac{mg}{L}}$ in order to minimize the negative impacts of elevated fluoride on human health. Dental fluorosis, the mildest condition caused by the consumption of fluoride, can begin with water concentrations above 0.9$\mathrm{\frac{mg}{L}}$. Skeletal fluorosis, a much more serious condition, can begin to develop with fluoride concentrations above 3$\mathrm{\frac{mg}{L}}$. Lastly, At concentrations above 10$\mathrm{\frac{mg}{L}}$ crippling skeletal fluorosis will begins to occur  [(WHO, 2004)](http://www.who.int/water_sanitation_health/dwq/chemicals/fluoride.pdf). The cases of dental fluorosis, the most mild indicator of excessive fluoride, varies across India, but has been shown to range from 13-91 percent depending on the demographic in question and their geographic location [(Arlappa et al., 2013)](http://www.ijrdh.com/files/11.Fluorosis.pdf). While there is no established average for fluoride in Indian groundwater, concentrations in some extreme cases have been measured to be as high as 20$\mathrm{\frac{mg}{L}}$ in some regions but most frequently are below 5$\mathrm{\frac{mg}{L}}$ [(LeChevallier and Au, 2004)](http://www.who.int/water_sanitation_health/publications/9241562552/en/).

The Bureau of Indian Standards have created water quality standards designed to protect the public from the adverse effects of fluoride. They have set the upper limit for fluoride at 1 $\mathrm{\frac{mg}{L}}$ and the permissible limit in the absence of an alternate source at 1.5 $\mathrm{\frac{mg}{L}}$ [(Bureau of Indian Standards, 2012)](http://archive.org/details/gov.in.is.10500.2012). The fluoride team has set their fluoride standards to the standards set by the Bureau of Indian Standards and therefore will be striving to achieve an effluent fluoride concentration of 1 $\mathrm{\frac{mg}{L}}$ or lower. The team will be experimenting with fluoride concentrations up to 20 $\mathrm{\frac{mg}{L}}$ in order to simulate the highest concentrations our systems may encounter out in the field.


## Previous Work
Discuss what is already known about your research area based on both external work and that of past AguaClara Teams. Connect your objectives with what is already known and explain what additional contribution you intend to make. Make sure to add APA formatted in-text citations. If you mention the author(s) in your sentence, you can simply give the year of publication.[(Logan et. al. 1987)](http://www.jstor.org/stable/pdf/25043431.pdf?acceptTC=true)

previous bench tests
adsorption model

The Spring 2018 fluoride team built a gravity-powered system. The constant head tanks for fluoride and coagulant ensure constant flow through the system. The heights of the constant head tanks were calculated using Bernoulli's equation:

$$ P_1 + \rho g \Delta h_1+ \frac{1}{2}\rho {v_1}^2 = P_2 + \rho g \Delta h_2+ \frac{1}{2}\rho {v_2}^2+ h_f $$

Details on design calculations can be found [here](https://github.com/AguaClara/fluoride/blob/master/Gravity%20Reactor.md). More information can be found in the Spring 2018 [report](https://github.com/AguaClara/fluoride/blob/master/FluorideReportSp18.md).

![gravity_schematic](https://github.com/AguaClara/fluoride/blob/master/fluoride%20report/Gravity%20Powered%20Reactor%20(2).jpg?raw=true)
Figure 1: Schematic for gravity-powered system. The constant head tanks for fluoride and PACl ensure constant flow through the system.

![gravity_reactor](https://github.com/AguaClara/fluoride/blob/master/fluoride%20report/labeledGravSystem.PNG?raw=true)
Figure 2: The fabricated gravity-powered system. The system includes a flocculator and a sedimentation tube.

The spring 2018 team also set up a bench experiment using ProCoDa. This experiment allowed for more precise control of the flowrates of water, fluoride, and PACl by using ProCoDa to control a set of pumps. The 2018 team also switched from using a sand filtration system to the reactor designed by the High Rate Sedimentation team.


## Methods
### Experimental Apparatus

The experimental apparatus included pumps, a coiled flocculator, and a sedimentation tube ([Figure 1](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Bench%20setup.png)). Two new sedimentation tubes were fabricated. Fabrication details are listed below, under the Manual section. Water flows into the system through the water pump. Fluoride and coagulant (PACl) are pumped into the system from their respective stock tanks. The pumps are operated by ProCoDA (Process Controller and Data Acquisition), which is a process control software created to automate pump control and generate datalogs ([Weber-Shirk, 2016](https://confluence.cornell.edu/display/AGUACLARA/ProCoDA)). The water, fluoride, and PACl mixture flows into the coiled flocculator. In the flocculator, PACl particles collide with fluoride ions, forming flocs. The mixture flows from the coiled flocculator to the sedimentation tube. Water flows up the sedimentation tube at a rate of 1.5 mm/s. This upflow velocity was used to calculate the necessary flow rate of water through the system. Calculations for the system flow rate can be found [here](https://github.com/AguaClara/fluoride/blob/master/SummerFluorideCalculations.md). Flocs are pumped from the sedimentation tube by a 1 rpm waste pump and exit through the floc weir. The treated water exits the sedimentation tube through the top where it flows to a sampling container. A sample is taken from the sampling container and the fluoride of the effluent water is measured by a fluoride probe.

![bench_setup](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Bench%20setup.png?raw=true)
Figure 1: The bench setup for the fluoride removal system.

The stock concentrations for fluoride were prepared to model the actual fluoride concentrations observed in India's groundwater. A range of 20 mg/L to 5 mg/L was tested, since the highest reported fluoride concentration in groundwater was 20 mg/L, while the average amount of fluoride among most regions was 5 mg/L ([Karthikeyan and Lakshanan, 2011](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Fluoride_book_chapter.pdf)). The goal was to reduce the fluoride influent concentration to 1.0 mg/L, to meet the India fluoride standards for drinking water ([Bhawan and Marg, 2009](https://github.com/AguaClara/fluoride)). In order to achieve the desired system concentrations of fluoride, the stock concentrations were prepared taking into account the flow rate of water through the system.

The following equation was used to calculate the system concentrations of fluoride and PACl:

$$ Q_{stock} * C_{stock} = Q_{sys} * C_{sys} $$

where $Q_{stock}$ is the flow rate out of the stock tank, $C_{stock}$ is the concentration of the stock tank containing fluoride or PACl stock, $Q_{sys}$ is the flow rate through the system, and $C_{sys}$ is the concentration of the fluoride or PACl through the system. Calculations for the fluoride and PACl stock concentrations can be found [here](https://github.com/AguaClara/fluoride/blob/master/SummerFluorideCalculations.md).


Table 1: Fluoride (F-) parameters. The desired fluoride system concentration was achieved by altering the fluoride pump speed. The fluoride stock concentration was kept constant at 2400 mg/L.
| F- Stock Concentration (mg/L) | F- Pump Speed (rpm) | F- System Concentration (mg/L) |
|:----------------------------- |:------------------- |:------------------------------ |
| 2400                             | 3                   | 3                              |
| 2400                             | 5                | 5                           |
| 2400                            |10                     | 10                               |
| 2400                              |15                     | 15                               |
| 2400                               |20                     |20                                |

Table 2: PACl parameters. Varying PACl system concentrations were tested at each of the fluoride system concentrations listed in the table above (Table 1). The desired PACl system concentration was achieved by altering the PACl pump speed, and the PACl stock concentration was kept constant.
| PACl Stock Concentration (mg/L) | PACl Pump Speed (rpm) | PACl System Concentration (mg/L) |
|:------------------------------- |:--------------------- |:-------------------------------- |
| 2400                            | 10                     | 10                                |
| 2400                            | 20                  | 20                             |
| 2400                            |30                       |30                                  |
| 2400                            |40                       |40                                  |
| 2400                                |50                       |50                                  |

### Fluoride Probe
The fluoride probe used was model FL43-0001 from Daigger Scientific, Inc. Previous teams had issues taking accurate measurements using this fluoride probe. The Spring 2018 fluoride subteam returned a fluoride probe and obtained a replacement.

![bench_setup](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/fluoride_probe.jpg?raw=true)
Figure 2: The fluoride probe used to measure effluent fluoride concentration.

The fluoride probe uses an ion-sensitive electrode ([Light, 1975](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/fluoride_paper.pdf)). When the fluoride probe is placed into a solution, the probe outputs a voltage reading. This voltage reading can then be converted to a fluoride concentration by using a calibration curve.

### Calibration Curve
The calibration curve was generated by formulating various concentrations of fluoride and measuring each sample with the fluoride probe (Table 3).

Table 3: The following standard concentrations were prepared by dilution of the 10000 ppm stock fluoride solution. The voltage was recorded from the fluoride probe.
| Standard (mg/L) | -log(Concentration) | Voltage |
|:--------------- |:------------------- |:------- |
| 0.1             | 10                  | 10      |
| 0.5             | 20                  | 20      |
| 1               | 30                  | 30      |
| 5               | 40                  | 40      |
| 10              | 50                  | 50      |
| 15              |                     |         |
| 20                |                     |         |

The calibration curve was generated by plotting  -log(Concentration) against voltage to generate a linear equation to model the relationship between voltage and concentration (Figure 3).

Figure 3: (add figure of calibration curve after finishing calibration) The linear equation that represents the relationship between voltage and concentration is (). The R-squared value is (). The slope is (), and the y-intercept is ().

```python
import matplotlib.pyplot as plt
plt.style.use('seaborn-whitegrid')
import numpy as np

fig = plt.figure()
ax = plt.axes()

ax.plot(x, x + 1)
plt.title("Calibration Curve")
plt.xlabel("Voltage")
plt.ylabel("Concentration (mg/L)");

```


### Gravity-Powered Apparatus
The gravity-powered apparatus was fabricated by the Spring 2018 fluoride team.

## Dye Test
dye testing



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


## Conclusions
Explain what you have learned and how that influences your next steps. Why does what you discovered matter to AguaClara?

Make sure that you defend your conclusions with facts and results.

## Future Work
Describe your plan of action for the next several weeks of research. Detail the next steps for this team. How can AguaClara use what you discovered for future projects? Your suggestions for challenges for future teams are most welcome. Should research in this area continue?

## Bibliography
ADA. (2017). Fluoride: Topical and Systemic Supplements. Retrieved from https://www.ada.org/en/member-center/oral-health-topics/fluoride-topical-and-systemic-supplements

Arlappa, N., Aatif Qureshi, I., and Srinivas, R. (2013). Fluorosis in India: an overview. Int J Res Dev
Health, 1(2).

Bureau of Indian Standards. (2012). IS 10500: Drinking water. Retrieved from http://archive.org/details/gov.in.is.10500.2012

Karthikeyan, B., Lakshanan, E. (2011). Fluoride in Groundwater: Causes, Implications and Mitigation Measures. *Fluoride Properties, Applications and Environmental Management*. 111-136. https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Fluoride_book_chapter.pdf

Light, T. (1975). Determination of Fluoride in Toothpaste Using an Ion-Selective Electrode. *Journal of Chemical Education, 52*(4), 247-250. https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/fluoride_paper.pdf

Mondal, D., Dutta, G., & Gupta, S. (2016). Inferring the fluoride hydrogeochemistry and effect of consuming fluoride-contaminated drinking water on human health in some endemic areas of Birbhum district, West Bengal. Environmental Geochemistry and Health, 38(2), 557–576. https://doi.org/10.1007/s10653-015-9743-7

NYC DEP. (2016). New York City 2016 Drinking Water Supply and Quality Report. Retrieved from http://www.nyc.gov/html/dep/pdf/wsstate16.pdf

Water-related diseases. (2016). World Health Organization. Retrieved from http://www.who.int/water_sanitation_health/diseases-risks/diseases/fluorosis/en/

Weber-Shirk, Monroe. (2016). AguaClara Confluence. Retrieved from https://confluence.cornell.edu/display/AGUACLARA/ProCoDA

WHO. (2004). Fluoride in Drinking-Water. Retrieved from http://www.who.int/water_sanitation_health/dwq/chemicals/fluoride.pdf

# Manual

## Fabrication Details
### Reactors
The reactor in both the bench system and the gravity powered system had multiple leakages. Therefore, two new reactors were fabricated by cutting out 2 sets of PVC pipes for the tube settler (90 cm) and floc weir (40 cm) according to [2017 Fall HRS team final report](https://confluence.cornell.edu/display/AGUACLARA/High+Rate+Sedimentation?preview=/327614520/350974719/high-rate-sedimentation%20(5).pdf).
Bent in the reactor was created using welder at 60 degrees from horizontal. Drill bit of 1/2 inch and thread of 1/4 inch were used. Holes were drilled into reactor for floc weir using circle saw and by setting the drill press at 55 degree angle. Floc weir pipe was then welded to the tube settler.

![sedtank](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/InkedSedtank_LI.jpg)
Figure 3: Reactor fabricated for both the bench system and gravity powered system

### Gravity Powered System
Valves as shown in figure 4 were added to the exits of the constant head tank and stock tank so that the both tanks can be removed separately for easier refills.

![Valves](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/Valves.jpg)
Figure 4: Valves added at the exits of both stock tank and constant head tank

  The

Flow rates
Height Adjustment

## Experimental Methods

### Set-up


### Bench System

### Gravity Powered System

Step 1.
* Put tasks in a sequential order.
* It is okay to have sub-lists.
  - Like this.

### Experiment


### Bench System

### Gravity Powered System

Step 1.

### Cleaning Procedure
Step 1.

## Experimental Checklist

### Bench System

### Gravity Powered System

## ProCoDA Method File
Use this section to explain your method file. This could be broken up into several components as shown below:

### States
Here, you should describe the function of each state in your method file, both in terms of its overall purpose and also in terms of the details that make it distinct from other states. For example:
\begin{itemize}
\item \underline{OFF} - Resting state of ProCoDA. All sensors, relays, and pumps are turned off.
\end{itemize}

### Set Points

![Setpoints](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/Setpoints.png)
Figure 6: Screenshot of set points in ProCoDA

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
