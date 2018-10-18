# Fluoride, Summer 2018
#### Ching Pang, Kevin Sarmiento, Cheer Tsang
This publication Fluoride, Summer 2018 was developed under Assistance Agreement No. SU-83695001 awarded by the U.S. Environmental Protection Agency to Cornell University. It has not been formally reviewed by EPA. The views expressed in this document are solely those of Ching Pang, Kevin Sarmiento, Cheer Tsang and do not necessarily reflect those of the Agency. EPA does not endorse any products or commercial services mentioned in this publication.

## Index
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Abstract](#abstract)
- [Introduction](#introduction)
- [Previous Work](#previous-work)
- [Methods](#methods)
  - [Experimental Apparatus](#experimental-apparatus)
  - [Procedure](#procedure)
  - [Fluoride Probe](#fluoride-probe)
  - [Calibration Curve](#calibration-curve)
  - [Sample Calculation](#sample-calculation)
- [Results](#results)
    - [Adsorption Model](#adsorption-model)
- [Future Work](#future-work)
- [Bibliography](#bibliography)
- [Manual](#manual)
  - [Fabrication Details](#fabrication-details)
    - [Sedimentation Tube](#sedimentation-tube)
    - [Gravity Powered System](#gravity-powered-system)
- [Experimental Methods](#experimental-methods)
  - [Electricity-Powered Fluoride Experiments](#electricity-powered-fluoride-experiments)
    - [Protocol for Running Just Water Through the Reactors](#protocol-for-running-just-water-through-the-reactors)
    - [Protocol for Start Up and Running of Reactors](#protocol-for-start-up-and-running-of-reactors)
    - [Experimental Checklist](#experimental-checklist)
    - [Cleaning Procedure](#cleaning-procedure)
    - [Fluoride Probe Calibration Procedure](#fluoride-probe-calibration-procedure)
  - [ProCoDA Method File](#procoda-method-file)
    - [States](#states)
    - [Set Points](#set-points)
- [Python Code](#python-code)
  - [Calculations for Water Pump Speed](#calculations-for-water-pump-speed)
  - [Calculations for Coagulant Pump Speed](#calculations-for-coagulant-pump-speed)
  - [Fluoride Pump Speed and Stock Concentration](#fluoride-pump-speed-and-stock-concentration)
  - [Calculations for Gravity Powered System](#calculations-for-gravity-powered-system)
<!-- END doctoc generated TOC please keep comment here to allow auto update -->


## Abstract

 Fluoride is a major contaminant in drinking water in many parts of India. The fluoride team's overarching goal is to create low cost, compact, and sustainable solutions to fluoride contamination in drinking water. The Summer 2018 team aims to continue and expand upon the work of previous teams by running experiments with both the pump-controlled system and the gravity powered system. The goal for the summer is to optimize the amount of coagulant needed to reduce the effluent fluoride concentration to 1 $\mathrm{\frac{mg}{L}}$, as per the fluoride standard in India and design an easily adjustable gravity powered system. In addition, the team aims to develop a simple user guide for the fluoride probe in order to maximize future teams' efficiency.

## Introduction

The recent expansion of AguaClara technology to new places around the world like India has uncovered new challenges and prompted new goals for AguaClara. In Honduras, where the majority of AguaClara plants have been constructed as of date, the source of water designated for purification comes from surface waters, such as rivers and lakes. Surface waters typically have a high amount of particulate matter and, as a result, also carry biological contaminants.
However, in India, 85% of the population drinks groundwater extracted from wells and aquifers. Contrast to surface water sources in Honduras, groundwater contains nearly no particulate matter, since many particles are naturally filtered out as the water percolates through the soil and rock material. While this natural filtration process is capable of removing particulate matter and reducing microorganisms, it also allows minerals and metals to leach into the water. Minerals that enter the water depend heavily on the types of parent rock material and soils found in the region.

India lies on one of the Fluoride Belts, which are expanses of land that are geologically rich in fluoride and have a much greater capacity to leach fluoride into groundwater. According to the World Health Organization, one of these belts stretches from Syria through Jordan, Egypt, Libya, Algeria, Sudan, and Kenya, while another starts in Turkey and goes through Iraq, Iran, Afghanistan, India, Northern Thailand, and China [(Water-related diseases, 2016)](http://www.who.int/water_sanitation_health/diseases-risks/diseases/fluorosis/en/). India contains about 14% of the total fluoride on the earth's crust, which inevitably leads the floride-rich groundwater [(Mondal, Dutta, & Gupta, 2016)](https://doi.org/10.1007/s10653-015-9743-7).

There are a number of public health implications associated with both underconsumption and overconsumption of fluoride. Fluoride is a common additive to municipal water systems in places such as the United States, where there is little to no fluoride naturally present in the water. Fluoride is added in order to prevent the onset of dental cavities. New York City, for example, adds fluoride to its water supply in order to achieve a concentration of 0.7 $\mathrm{\frac{mg}{L}}$ in its effluent supply [(NYC DEP, 2016)](http://www.nyc.gov/html/dep/pdf/wsstate16.pdf). The American Dental Association has set the recommended concentration of fluoride in drinking water to 0.7 $\mathrm{\frac{mg}{L}}$ for the prevention of dental cavities [(ADA, 2017)](https://www.ada.org/en/member-center/oral-health-topics/fluoride-topical-and-systemic-supplements). There are, however, a number of health risks associated with the consumption of fluoride at higher concentrations.

The World Health Organization has set an absolute limit on the concentration of fluoride in drinking water to 1.5 $\mathrm{\frac{mg}{L}}$ in order to minimize the negative impacts of elevated fluoride on human health. Dental fluorosis, the mildest condition caused by the consumption of fluoride, can begin with water concentrations above 0.9 $\mathrm{\frac{mg}{L}}$. Skeletal fluorosis, a much more serious condition, can begin to develop with fluoride concentrations above 3 $\mathrm{\frac{mg}{L}}$. Lastly, at concentrations above 10 $\mathrm{\frac{mg}{L}}$, crippling skeletal fluorosis will begins to occur  [(WHO, 2004)](http://www.who.int/water_sanitation_health/dwq/chemicals/fluoride.pdf). The cases of dental fluorosis, the mildest indicator of excessive fluoride, varies across India, but has been shown to range from 13-91 percent, depending on the demographic in question and geographic location [(Arlappa et al., 2013)](http://www.ijrdh.com/files/11.Fluorosis.pdf). While there is no established average for fluoride in Indian groundwater, concentrations in some extreme cases have been measured to be as high as 20 $\mathrm{\frac{mg}{L}}$ in some regions, but most frequently are below 5 $\mathrm{\frac{mg}{L}}$ [(LeChevallier and Au, 2004)](http://www.who.int/water_sanitation_health/publications/9241562552/en/).

The Bureau of Indian Standards has created water quality standards designed to protect the public from the adverse effects of fluoride. They have set the upper limit for fluoride at 1 $\mathrm{\frac{mg}{L}}$ and the permissible limit in the absence of an alternate source at 1.5 $\mathrm{\frac{mg}{L}}$ [(Bureau of Indian Standards, 2012)](http://archive.org/details/gov.in.is.10500.2012). AguaClara's fluoride subteam has set its fluoride standards to match the standards set by the Bureau of Indian Standards and therefore will be striving to achieve an effluent fluoride concentration of 1 $\mathrm{\frac{mg}{L}}$ or lower. The team will be experimenting with fluoride concentrations up to 20 $\mathrm{\frac{mg}{L}}$ in order to simulate the highest concentrations our systems may encounter out in the field.

The objectives for the 2018 Summer Fluoride team are:
1. Create an adsorption model to determine the optimal PACl dosage for varying concentrations of fluoride.
2. Fabricate a user-friendly gravity-powered fluoride removal system that will be used for research. The goal is for the system to be easily adjustable so that various parameters can be tested.


## Previous Work

The Spring 2018 team set up a bench experiment that allowed for precise control of the flow rates of water, fluoride, and coagulant. Polyaluminum chloride (PACl) was the coagulant used in the system. The 2018 team also switched from using a sand filtration system to a flocculation/sedimentation process, which included a tube settler designed by the High Rate Sedimentation team. The sand filtration posed many issues, such as an increase in headloss over time due to the buildup of particles in the filter, which caused clogging. Thus, the flocculation/sedimentation process traditionally used in drinking water treatment was proposed as a possible fluoride removal method.

The team ran several tests with various influent concentrations of fluoride and PACl to determine the optimal PACl dosage to treat a given concentration on influent fluoride. The target effluent fluoride was 1.5 mg/L, based on standards set by the World Health Organization (WHO). At the maximum PACl dosage, the reactor became clogged with a fluidized bed, due to insufficient shear to break up the flocs. The team suggested adding a second reactor to decrease the maximum PACl required. The results have been thus far inconclusive, and the team suggested that the source of error may be a faulty fluoride probe. The team then ordered a replacement probe ([Akpan, 2018](https://github.com/AguaClara/fluoride/blob/master/FluorideReportSp18.md)).

In addition, the Spring 2018 fluoride team built a gravity-powered system. The constant head tanks for fluoride and coagulant ensure constant flow through the system. The heights of the constant head tanks were calculated using Bernoulli's equation:

$$ P_1 + \rho g \Delta h_1+ \frac{1}{2}\rho {v_1}^2 = P_2 + \rho g \Delta h_2+ \frac{1}{2}\rho {v_2}^2+ h_f $$

Details on design calculations can be found [here](https://github.com/AguaClara/fluoride/blob/master/Gravity%20Reactor.md). More information can be found in the Spring 2018 [report](https://github.com/AguaClara/fluoride/blob/master/FluorideReportSp18.md).

![gravity_schematic](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Bench_setup_new.png?raw=true)
Figure 1: Schematic for gravity-powered system. The constant head tanks for fluoride and PACl ensure constant flow through the system.

![gravity_reactor](https://github.com/AguaClara/fluoride/blob/master/fluoride%20report/labeledGravSystem.PNG?raw=true)
Figure 2: The fabricated gravity-powered system. The system includes a flocculator and a sedimentation tube.


## Methods
### Experimental Apparatus

The experimental apparatus included pumps, a coiled flocculator, and a sedimentation tube ([Figure 1](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Bench%20setup.png)). Two new sedimentation tubes were fabricated. Fabrication details are listed under the Manual section. Water flows into the system through the water pump. Fluoride and coagulant (PACl) are pumped into the system from their respective stock tanks. The pumps are operated by ProCoDA (Process Controller and Data Acquisition), which is a process control software created to automate pump control and generate datalogs ([Weber-Shirk, 2016](https://confluence.cornell.edu/display/AGUACLARA/ProCoDA)). The water, fluoride, and PACl mixture flows into the coiled flocculator. In the flocculator, PACl particles collide with fluoride ions, forming flocs. The mixture flows from the coiled flocculator to the sedimentation tube. Water flows up the sedimentation tube at a rate of 1.5 mm/s. This upflow velocity was used to calculate the necessary flow rate of water through the system. Calculations for the system flow rate can be found [here](https://github.com/AguaClara/fluoride/blob/master/SummerFluorideCalculations.md). Flocs are pumped from the sedimentation tube by a 1 rpm waste pump and exit through the floc weir. The treated water exits the sedimentation tube through the top where it a sample is taken, and the fluoride of the effluent water is measured by a fluoride probe.

![bench_schematic](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Bench_setup_new.png?raw=true)
Figure 3: A schematic drawing of the bench setup for the fluoride removal system.

![bench_setup](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/Labeled_bench_setup.jpg)
Figure 4: Current pump powered bench setup for the fluoride removal system.


### Procedure

The stock concentration for fluoride was prepared to model the actual fluoride concentrations observed in India's groundwater. A range of 20 mg/L to 5 mg/L was tested, since the highest reported fluoride concentration in groundwater was 20 mg/L, while the average amount of fluoride among most regions was 5 mg/L ([Karthikeyan and Lakshanan, 2011](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Fluoride_book_chapter.pdf)). The goal was to reduce the fluoride influent concentration to 1.0 mg/L, to meet the India fluoride standards for drinking water ([Bhawan and Marg, 2009](https://github.com/AguaClara/fluoride)).

The stock fluoride bottle was made in way that allows for a range of fluoride concentration in the entire system by only adjusting the pump speed. This reduced the need for a different stock for each desired concentration of fluoride in the entire system.  

The following equation was used to calculate the system concentrations of fluoride and PACl:

$$ Q_{stock} * C_{stock} = Q_{sys} * C_{sys} $$

where $Q_{stock}$ is the flow rate out of the stock tank, $C_{stock}$ is the concentration of the stock tank containing fluoride or PACl stock, $Q_{sys}$ is the flow rate through the system, and $C_{sys}$ is the concentration of the fluoride or PACl through the system. Calculations for the fluoride and PACl stock concentrations can be found below.

```python
#fluoride calculations
#Calculation for the system flowrate are needed in order to calculate the required fluoride stock concentration that will produce the needed system concentrations of fluoride  
#D=diameter of sed tube
D=(1)*u.inch
D=D.to(u.m)
A=np.pi*(D**2)/4
print(A)
v=(0.0015)*(u.m/u.s)
#v=desired upflow velocity in sed tube
Q=(A*v) #Q=system flowrate
print(Q)
Q=Q.to((u.milliliter)/(u.second))
print(Q)

#Assume Qstock, Qsystem and Csystem

pump_speed = 3*(u.rpm)
#yellow_blue = 0.149*(u.milliliter/u.revolutions)
#yb_flowrate = yellow_blue.to(u.liter/u.revolutions)*(pump_speed).to(u.revolutions/u.s)
orange_yellow = 0.019*(u.milliliter/u.revolutions)
oy_flowrate = orange_yellow.to(u.liter/u.revolutions)*(pump_speed).to(u.revolutions/u.s)

print('The fluoride flow rate is: '+str((oy_flowrate).to(u.milliliter/u.s))) #Qstock . This is what is entered into ProCoDa under fluoride flowrate for controlling the fluoride pump.

Q_sys=Q.to((u.liter)/(u.second)) #From Calculations for Water Pump speed and assume oy_flowrate is negligible for now
Q_stock = oy_flowrate # setting Q_stock = oy_flowrate makes controlling the pumps rather simple. If the desired concentration in the system is 5mg/L of fluoride then the pump speed to achieve that is 5 RPM

C_sys = 3*(u.mg/u.L) #user input desired concentration of F- in the system.

C_stock= (Q_sys*C_sys)/Q_stock
print('The fluoride concentration in the stock is: ' +str(C_stock))
#The equation M1V1=M2V2 is used below to obtain volume of fluoride stock needed
M_superstock = 10000 * (u.mg/u.L) #concentration of fluoride superstock purchased.  
M_stock = C_stock
V_stock = 0.5 * u.L #total volume of the stock (water+fluoride)
V_superstock= (M_stock*V_stock)/M_superstock
print('The fluoride superstock volume in the stock is: ' +str((V_superstock).to(u.milliliter)))
V_water=V_stock-V_superstock
print('The water volume in the stock is : ' +str((V_water).to(u.milliliter)))

percent_flow = (oy_flowrate/Q_sys)*100
print('The percent flow rate of fluoride/total flow through system: '+str(percent_flow)+' %.')

total_flowrate = oy_flowrate_PACl + oy_flowrate + Q
print('The total flowrate through the system is: '+str(total_flowrate))
water_flowrate = 0.76 * (u.milliliter/u.s) - (oy_flowrate + oy_flowrate_PACl)
print('The actual water pump flow rate required is: '+str(water_flowrate))
```

```python
#PACl calculations are the same as that of fluoride with the only difference that the superstocks are different. So each requires different amount of susperstock and water in order to achieve the desired 2400mg/L concentration.  

#Just as the previous calculations, the system flowrate are needed in order to calculate the required PACl stock concentration that will produce the desired system concentrations of PACl
#D=diameter of sed tube
D=(1)*u.inch
D=D.to(u.m)
A=np.pi*(D**2)/4
print(A)
v=(0.0015)*(u.m/u.s)
#v=desired upflow velocity in sed tube
Q=(A*v) #Q=system flowrate
print(Q)
Q=Q.to((u.milliliter)/(u.second))
print(Q)

#Aim for 6.5 mg/L of PAC the lowest according to Github Issues
pump_speed_PACl = 30*(u.rpm)
#orange_yellow is a type of small diameter tubing used on the pump
orange_yellow = 0.019*(u.milliliter/u.revolutions)
oy_flowrate_PACl = orange_yellow.to(u.liter/u.revolutions)*(pump_speed_PACl).to(u.revolutions/u.s)

print('The PACl flow rate is: '+str((oy_flowrate_PACl).to(u.milliliter/u.s))) #Qstock

Q_sys=Q.to((u.liter)/(u.second)) #From Calculations for Water Pump speed and assume oy_flowrate is negligible for now
Q_stock_PACl = oy_flowrate_PACl
C_sys_PACl = 30*(u.mg/u.L) #user input desired concentration of PACl in the system. Our tests use between 10mg/L and 50mg/L of PACl.

C_stock_PACl = (Q_sys*C_sys_PACl)/Q_stock_PACl
print('The PACl concentration in the stock is: ' +str(C_stock_PACl))
#The equation M1V1=M2V2 is used to obtain the volume of PACl superstock needed
M_superstock_PACl = (70.28 * (u.g/u.L)).to(u.mg/u.L) #concentration of PACl provided to AguaClara from the Ithaca Water Treatment facility.
M_stock_PACl = C_stock_PACl
V_stock_PACl = 0.5 * u.L #total volume of the stock (water+PACl)
V_superstock_PACl = (M_stock_PACl*V_stock_PACl)/M_superstock_PACl
print('The PACl superstock volume in the stock is: ' +str((V_superstock_PACl).to(u.milliliter)))
V_water_PACl = V_stock_PACl-V_superstock_PACl
print('The water volume in the PACl stock is : ' +str((V_water_PACl).to(u.milliliter)))
```

Table 1: Fluoride (F-) parameters. The desired fluoride system concentration was achieved by altering the fluoride pump speed. The fluoride stock concentration was kept constant at 2400 mg/L.

| F- Stock Concentration (mg/L) | F- Pump Speed (rpm) | F- System Concentration (mg/L) |
|:----------------------------- |:------------------- |:------------------------------ |
| 2400                          | 3                   | 3                              |
| 2400                          | 5                   | 5                              |
| 2400                          | 10                  | 10                             |
| 2400                          | 15                  | 15                             |
| 2400                          | 20                  | 20                             |


Table 2: PACl parameters. Varying PACl system concentrations were tested at each of the fluoride system concentrations listed in the table above (Table 1). The desired PACl system concentration was achieved by altering the PACl pump speed, and the PACl stock concentration was kept constant.

| PACl Stock Concentration (mg/L) | PACl Pump Speed (rpm) | PACl System Concentration (mg/L) |
|:------------------------------- |:--------------------- |:-------------------------------- |
| 2400                            | 10                     | 10                                |
| 2400                            | 20                  | 20                             |
| 2400                            |30                       |30                                  |
| 2400                            |40                       |40                                  |
| 2400                                |50                       |50                                  |



Samples were taken at two different locations throughout the experiment. One at the influent, before treatment with PACl, and another at the effluent, after treatment with PACl. Samples were taken every 15 minutes. The calculated residence time of the pump powered system was of 13.22 minutes therefore the first sample was taken 15 minutes after beginning the experiment to give the system enough time to reach the desired fluoride concentration. The residence time is the amount of time a fluoride ion takes to be transported from the start of the system, when it enters the coiled flocculator, to the system effluent after the sedimentation tube. Residence time calculations can be found [here](https://github.com/AguaClara/fluoride/blob/master/residence_time.md).

### Fluoride Probe
The fluoride probe used was model FL43-0001 from Daigger Scientific, Inc. However, previous teams had issues taking accurate measurements using this fluoride probe. The Spring 2018 fluoride subteam returned a probe and obtained a replacement, which is the one the Summer 2018 team has used. Manual for operating the probe can be found [here](https://github.com/AguaClara/fluoride/wiki/Fluoride-Probe-Manual).

![fluoride_probe](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/fluoride_probe.jpg?raw=true)
Figure 4: The fluoride probe used to measure effluent fluoride concentration.

The fluoride probe uses an ion-sensitive electrode ([Light, 1975](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/fluoride_paper.pdf)). When the fluoride probe is placed in a fluoride solution, the probe outputs a voltage reading. This voltage reading can then be converted to a fluoride concentration by first creating a calibration curve and comparing the output voltage to the calibration curve.

While the FL43-0001 probe is still functional, the team decided to order a [new fluoride probe](https://github.com/AguaClara/fluoride/issues/59). This was necessary considering that for the upcoming Fall 2018 semester there will be two active fluoride teams. One team will be running tests with the pump station while the other will be running tests on the gravity system. Each team will need to test their samples for fluoride. The second probe, a Cole-Parmer Ion-Selective Electrode (ISE) was ordered at the end of the summer. Additionally, a third fluoride probe is also recommended in order to prevent future loss of time due to delays caused by non-functional probes. This should be one of the first tasks of the Fall 2018 fluoride team, to search and purchase a third backup probe.


### Calibration Curve
The calibration curve was generated by formulating various concentrations of fluoride and measuring each sample with the fluoride probe (Table 3).

Table 3: The following standard concentrations were prepared by dilution of the 10000 ppm stock fluoride solution. The voltage was recorded from the fluoride probe. Data in table below is from the calibration curve generated on 7/19/2018.

| Standard (mg/L) | -log(Concentration) | Voltage |
|:--------------- |:------------------- |:------- |
| 0.1             | 1                   | 0.0818       |
| 0.3             | 0.5228787453        | 0.0694       |
| 0.5             | 0.3010299957        | 0.0621       |
| 1               | 0                   | 0.0478       |
| 3               | -0.4771212547       | 0.0223       |
| 5               | -0.6989700043       | 0.0102       |
| 10              | -1                  | -0.0045      |
| 15              | -1.176091259        | -0.009       |
| 20              | -1.301029996        | -0.0166      |

The calibration curve was generated by plotting  voltage against -log(Concentration) to generate a linear equation to model the relationship between voltage and concentration (Figure 3).

### Sample Calculation
The probe was re-calibrated for each experiment trial, and a new calibration curve was graphed for each trial. Below is a sample calculation from one experiment trial. Documentation on how to generate a calibration curve using Python can be found [here](https://github.com/AguaClara/aguaclara_research/wiki/Plotting-and-Linear-Regression-in-Python-(in-progress)). The data for the calibration curves generated for each experiment can be found [here](https://docs.google.com/spreadsheets/d/1Qdzn8rtu0ubeyHFeoxpHNJPTBkcbFvO21DLpOUB-Flc/edit?usp=sharing).  

```python
import matplotlib.pyplot as plt
%matplotlib inline
import numpy as np
from scipy import stats

#Replace coordinates here with your data. Make as many coordinates as necessary.

#x coordinates are the known fluoride concentrations of the prepared fluoride standards
#y coordinates are the voltages recorded by the fluoride probe
#the negative logarithm of the voltage is taken to generate a linear curve

data_points = np.array([[0.1, 0.0818],
                       [0.3,0.0694],
                       [0.5,0.0621],
                       [1,0.0478],
                       [3,0.0223],
                       [5,0.0102],
                       [10,-0.0045],
                       [15,-0.009],
                       [20,-0.0166]])

x_points = -np.log10(data_points[:,0])
y_points = data_points[:,1] # You can perform operations on your data here such as np.log10(data_points[:,1])

linreg = stats.linregress(x_points, y_points)
slope, intercept, r_value = linreg[0:3]

start = x_points[-1] # Change as desired
end = x_points[0] # last element plus one; change as desired
plt.plot(x_points, y_points, 'o')
plt.plot(np.arange(start,end,0.1), np.arange(start, end,0.1)*slope + intercept)
plt.xlabel('-log(Concentration) (mg/L)')
plt.ylabel('Voltage')
plt.title('Calibration Curve')
plt.minorticks_on()
plt.grid(which = 'major')
plt.grid(which = 'minor')
plt.savefig("filename.png",dpi=1000)
plt.show()


print("Slope:", slope)
print("Intercept:", intercept)
print("R-squared:", r_value ** 2)



```
![calibration_curve](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/calibration_curve.png?raw=true)
Figure 5: The linear relationship between voltage and concentration. The R-squared value is 0.9900. The slope is 0.04529, and the y-intercept is 0.04352.


## Results
Experiments were run with varying concentrations of fluoride and PACl. In each case, the effluent fluoride concentration was lower than the influent fluoride concentration, which indicated that the flocculation/sedimentation system was effective in removing fluoride.

Table 4: Data taken on 7/25/2018. The time, influent fluoride concentration, and effluent fluoride concentration were recorded at each 15 minute interval. The fluoride dosage was 10 mg/L and the PACl dosage was 50 mg/L.

| Time (hr) | Fluoride (mg/L) | PACl (mg/L) | Influent Fluoride (mg/L)   | Effluent Fluoride (mg/L)  |
|:-----|:----|:--- | --- | --- |
| 0.25 | 10  | 50  | 13.42056163    | 1.642056825    |
| 0.5  | 10  | 50  | 12.06523927    | 3.369977473    |
| 1.0  | 10  | 50  | 11.37457308    | 3.316232356    |
| 1.25 | 10  | 50  | 10.95578916    | 3.211299867    |
| 1.5  | 10  | 50  | 10.21852321    | 3.228555153    |
| 2.0  | 10  | 50  | 10.27343043    | 3.613121185    |
| 2.25 | 10  | 50  | 8.4256534      | 3.812027396    |
| 2.5  | 10  | 50  | 7.528860869    | 3.536495699    |
| 3    | 10  | 50  | 6.207900192    | 3.832510573    |

There are however many inconsistencies that have been observed in the data. For example, when testing the influent fluoride concentration, before the addition of PACl, the fluoride readings with the probe do not always match what the calculated fluoride system concentration should be.


### Adsorption Model
The results of the experiments were plotted to generate an adsorption model. Surface adsorption is the process of molecules or ions adhering to a solid surface. There are two general types of adsorption: physisorption and chemisorption. In physisorption, the adsorbate binds to a surface via loose, non-specific van der Waals interactions. This process allows multilayer binding and can be disrupted by increasing temperatures. The process of chemiadsorption is like a chemical reaction, allowing more specific binding, which only allows monolayer binding. Chemiadsorption can be modeled by the Langmuir Isotherm.

The Langmuir Isotherm has three assumptions:
1. "The surface of the adsorbant is in contact with a solution containing an
adsorbate which is strongly attracted to the surface."
2. "The surface has a specific number of sites where the solute molecules
can be adsorbed."
3. "The adsorption involves the attachment of only one layer of molecules
to the surface, i. e. monolayer adsorption." ([Altig, 2018](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Langmuir-Isotherm.pdf))

In linear form, the Langmuir Isotherm is modeled by the equation:

$$ \frac{C_e}{q_e} = \frac{1}{q_e}C_e+\frac{1}{K_L\cdot q_m} $$

where $C_e$ is the equilibrium concentration of the adsorbant, $q_e$ is the amount adsorbed at equilibrium, and $K_L$ and $q_m$ are Langmuir constants which are related to adsorption capacity and energy of adsorption.

Thus, the amount of fluoride adsorbed by the PACl was calculated by the following equation:

$$ W  = \frac{inital fluoride - final fluoride}{mass of PACl} $$

Table 5: Data taken on 7/25/2018. The amount of fluoride adsorbed (W) was plotted against the effluent fluoride.

| Influent Fluoride (mg/L)| Effluent Fluoride (mg/L) | W |
|:-----|:-----|:----|
| 13.42056163    | 1.642056825 | 0.235570096  |
| 12.06523927    | 3.369977473  | 0.173905236  |
| 11.37457308    | 3.316232356  | 0.161166814  |
| 10.95578916    | 3.211299867 | 0.154889786  |
| 10.21852321    | 3.228555153  | 0.139799361  |
| 10.27343043    | 3.613121185  | 0.133206185  |
| 8.4256534      | 3.812027396 | 0.09227252  |
| 7.528860869    | 3.536495699  | 0.079847303  |
| 6.207900192    | 3.832510573    | 0.047507792  |


The complete data for each experiment can be found [here](https://docs.google.com/spreadsheets/d/1Qdzn8rtu0ubeyHFeoxpHNJPTBkcbFvO21DLpOUB-Flc/edit?usp=sharing). This data was graphed to create the adsorption model (Figure 6).

![adsorption_linear](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/adsorption_linear.png?raw=true)

Figure 6: Linear adsorption model fitted to Langmuir Isotherm.

![adsorption_model](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/adsorption_model.png?raw=true)

Figure 7: Langmuir adsorption model, with outliers and inconsistencies removed. The points in blue contain all data from experiments run with 5 mg/L influent concentration of fluoride. The points in green are 15 mg/L influent fluoride, and the points in orange are 10 mg/L influent fluoride.

## Future Work
#### Automated Benchtop System

For the pump-powered (automated) system, experiments with 3 mg/L and 20 mg/L should be run to improve the accuracy of the adsorption model. Once these experiments have been completed, the adsorption model should be analyzed for trends at different PACl and fluoride concentrations.

An additional task is to test different upflow velocities. It was noted that the coagulant formed a gel at the bottom of the sedimentation tube after running the experiment for several hours, thus causing a buildup of coagulant, which obstructed the upflow velocity. A future goal should be to determine an optimal upflow velocity through the sedimentation tube that minimizes the buildup of gel.

The formation of floc blanket in fluoride tests is more difficult than in clay mixture tests. However, the importance of floc blanket in fluoride removal tests is still unknown. Therefore, the height of the floc blanket should be further investigated to see whether it affects fluoride removal efficiency directly or just floc removal.

The data graphed for the Langmuir isotherm has much variability, in which there was particular vertical trends seen in the graph. Future teams should investigate into the data trends and compare that from the gravity powered system.

#### Gravity Powered System

The gravity powered system has been modified so that it allows for easy adjustments to both fluoride flow rate and PACl flow rate. However, no tests have been done using this system yet. The gravity powered fluoride removal team should work to optimize the flow rate of both of these variables in order to achieve the desired effluent fluoride concentration of 1 mg/L fluoride.

Future teams should also research on how to operate the system based on the findings of the automated system. A future goal should be to optimize the system so that it is compact, easy to transport, and easy to use. A standard operation manual should be developed so that the system can be tested in Honduras or India. The future team should also research options on how the system should be field-tested.

Another goal is to research options on how to handle the fluoride-coagulant waste that exits the fluoride-removal system. One possible option is to concentrate the waste stream. Future teams should consider how the waste should be handled on-site in the communities where the fluoride-removal systems will be implemented.

##Conclusion
The summer 2018 fluoride team focused on creating an adsorption model by testing various fluoride and PACl concentrations. The team also worked on fabricating a gravity-powered system that will be used for research in the field.

## Bibliography
ADA. (2017). Fluoride: Topical and Systemic Supplements. Retrieved from https://www.ada.org/en/member-center/oral-health-topics/fluoride-topical-and-systemic-supplements

Akpan, P. Mehrabyan, T. Sausele, D., Fluoride, Spring 2018. Retrieved from https://github.com/AguaClara/fluoride/blob/master/FluorideReportSp18.md

Altig, Jeff. (2018). The Langmuir Adsorption Isotherm. Retrieved from https://infohost.nmt.edu/~jaltig/Langmuir.pdf

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
### Sedimentation Tube
The sedimentation tube in both the bench system and the gravity powered system had multiple leakages. Therefore, two new tube settlers were fabricated by cutting out 2 sets of PVC pipes for the tube settler (90 cm) and floc weir (40 cm) according to [2017 Fall HRS team final report](https://confluence.cornell.edu/display/AGUACLARA/High+Rate+Sedimentation?preview=/327614520/350974719/high-rate-sedimentation%20(5).pdf).
60 degree bends from the horizontal were created using a welder. Drill bit of 1/2 inch and thread of 1/4 inch were used. Holes were drilled into reactor for floc weir using circle saw and by setting the drill press at 55 degree angle. The floc weir pipe was then welded to the tube settler.


![sedtank](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Sedtank_labeled.jpg?raw=true)
Figure 5: Reactor fabricated for both the bench system and gravity powered system.

### Gravity Powered System
Fixes to the gravity powered system from the [2018 Spring fluoride removal team final report](https://github.com/AguaClara/fluoride/blob/master/FluorideReportSp18.md) were made which included fixing several leaks throughout the apparatus. The newly fabricated reactor was installed to fix the leakages. Valves as shown in figure 4 were also added to the exits of the constant head tank and stock tank so that the both tanks can be easily removed for refilling.

![Valves](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/Valves.jpg)
Figure 4: Valves added at the exits of both stock tank and constant head tank

#### Making Gravity Powered System Adjustable

Further improvements to the gravity powered system which allows for easier adjustments to fluoride and PACl flowrates were made. This was accomplished by installing sliding tracks onto the body of the gravity system frame. Additionally all components were lowered in order to place the whole setup on top of a lab bench in order to conserve space in the lab.
![Gravity powered reactor](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Gravity_reactor_labeled_edit.jpg?raw=true)
Figure 5: Modified gravity powered reactor shown with 3 adjustable sliders.

Figure 6 shows the two adjustable platforms that hold PACl. The top platform has a scale attached to it in order to accurately measure the weight of PACl at different time intervals. This information can then be used to calculate the flowrate of PACl into the system more accurately than previously done before. The top 1L PACl tank feeds the bottom 1L PACl constant head tank. Their hights can be adjusted inorder to achieve the desired PACl system concentration.

![PACl adjustable tanks](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Gravity_reactor_PACl_adjustable_edit.jpg?raw=true)
Figure 6: Height adjustable PACl platforms used to easily adjust system concentration of PACl.

A third adjustable slider was added to the frame of the gravity powered system. This last piece allows for easy control of the system flowrate. By adjusting the height of the effluent point relative to the top of the constant fluoride head tank the system flowrate can be easily adjusted.

![System Flowrate Adjustment](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Gravity_reactor_sedtank_labeled.jpg?raw=true)
Figure 7: Slider allows for easy and fast adjustment of the system flowrate of the gravity powered system.  


## Experimental Methods

### Electricity-Powered Fluoride Experiments
The following are improvised based on protocols used for past semesters' experimentation.


#### Protocol for Running Just Water Through the Reactors

1. Open tap water valve and turn off the fluoride pump as to not pump fluoride into the system during backwash
2. Close the waste line
3. Turn on Just Water process in ProCoDA and fill system completely with water
4. Continue to run water at high velocity for at least 15 minutes

#### Protocol for Start Up and Running of Reactors
1. Fill stock tanks with appropriate concentration of PACl and fluoride, and make sure to have enough stock to run for 3 hours
2. Calculate the flow rates of the PACl and fluoride pumps from the Python file and run the pumps at the appropriate RPM using ProCoDA
3. Run the waste pump at the appropriate RPM as calculated from ProCoDA.
4. Calibrate the fluoride probes and record the initial concentration of fluoride in the sample bottle

#### Experimental Checklist:
##### Before starting test
1. Waste line is opened. (System will explode if this is not open)
2. No leaks anywhere in system
3. Ensure that all collection valves are closed and that the main line valves are open. Failure to do so can cause sed tank to explode
![System_Valves](https://github.com/AguaClara/Fluoride-Auto/blob/master/Summer%202018%20fluoride%20report/Influent_valves_edit.JPG?raw=true)
Figure 8. Main line valve and collection valves

4. Check PACl and Fluoride stock containers and refill them when necessary
5. Make sure that lids are on the containers but not tightly sealed in order to prevent negative pressure from crushing the stock containers
6. Turn on magnetic stir plates under the stock containers (NOT THE HEAT)
![Stir](https://github.com/AguaClara/Fluoride-Auto/blob/master/Summer%202018%20fluoride%20report/Stock_stir.jpg?raw=true)
Figure 9. PACl and fluoride stock on stir

7. Turn on all pumps and set them to run at the desired RPM (Check ProCoDA)
8. Set all pumps to run in the correct direction (in the direction of the flocculator and reactor)
9. Write a text file in ProCoDA saying "Start Test" with appropriate descriptors including fluoride concentration, PACl concentration, upflow velocity, etc. and then change the process to the ON state.

##### During test
7. Recheck everything periodically to ensure it is running how it should be and that there are no water leaks
8. Take an influent and effluent sample every 15 minutes by using the valve after fluoride and before coagulant is added (influent) and after the sedimentation tube (effluent). Remember to not close both main line valve and collection valves at the same time. Doing so will cause the system to explode.
![Influent_sampling](https://github.com/AguaClara/Fluoride-Auto/blob/master/Summer%202018%20fluoride%20report/Influent_collection.jpg?raw=true)
Figure 10. Sampling of influent fluoride concentration  

![Effluent_sampling](https://github.com/AguaClara/Fluoride-Auto/blob/master/Summer%202018%20fluoride%20report/Effluent_collection.jpg?raw=true)
Figure 11. Sampling of effluent fluoride concentration

##### End of test
8. Change the process to the OFF state.
9. Clean the reactor using the "Cleaning  Procedure" after the experiment is completed.

#### Cleaning Procedure
1. Follow protocol for "Running Just Water Through the Reactors"
2. Unplug the waste line and allow the water to drain
3. Put a piece of sponge in the tube between the flocculator and PACl insert.
4. Run a high velocity jet through the tube to purge the flocculator.
5. Drain both reactors through the valves at the bottom of the reactors.
. Flush water through both reactors again and let it drain.

#### Fluoride Probe Calibration Procedure
1. Make the stock calibration concentrations of 0.1 $\mathrm{\frac{mg}{L}}$, 0.3 $\mathrm{\frac{mg}{L}}$, 0.5 $\mathrm{\frac{mg}{L}}$, 1 $\mathrm{\frac{mg}{L}}$, 3 $\mathrm{\frac{mg}{L}}$, 5  $\mathrm{\frac{mg}{L}}$, 10 $\mathrm{\frac{mg}{L}}$, 15 $\mathrm{\frac{mg}{L}}$,and 20 $\mathrm{\frac{mg}{L}}$ in small bottles. Individually pipette fluoride stocks into all four bottles, do not use serial dilutions.
2. Rinse the fluoride probe with DI water and carefully dab the end of the probe on a Kimwipe. If any sediments from prior experiments remain, rub off with polishing
3. Insert the probe into one of the calibration solutions.
4. Swirl the probe around, then let settle. Record the voltage once it reaches a steady state
5. Make sure to record the voltage at the minimum voltage (the voltage will spike first and eventually reach a steady state voltage before increasing again). ![Fluoride Voltage readings on ProCoDa](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/ProCoDa_fluoride_probe_calibration.JPG?raw=true)
Figure 6: Voltage reading of fluoride sample on ProCoDa

6. Repeat with the other fluoride concentrations and record the values in Google Docs (labeled "Fluoride Calibration"). [Summer Fluoride Calibration](https://docs.google.com/spreadsheets/d/1Qdzn8rtu0ubeyHFeoxpHNJPTBkcbFvO21DLpOUB-Flc/edit#gid=0)
7. The R squared value, slope, and y-intercept will be updated as the voltages are updated (make sure the R squared value is at least .99 to ensure accurate fluoride calibrations).
8. If R squared value is not 0.99, rinse let settle in standard solution (50% TISAB and 50% DI water), then rinse thoroughly with DI water. Sand with polishing strip, and repeat procedure, gently shaking probe up and down before first calibration measurement.
<!--Add photos! -->
### ProCoDA Method File

ProCoDA is a process control system that was developed by Monroe Weber-Shirk in order to set process parameters through a computerized system. It can be adjusted to different system states that control the system pumps depending on what flow rates are desired. Additionally, ProCoDA collects the data from probes, allowing for compilation of dye concentration data.

To begin the ProCoDA method file, three states were made: ON and OFF and Just Water. In the OFF state, all the valves were closed and no pumps were on. In the ON state, all the pumps were ON and all valves were opened, in the Just Water state, only the water valve was open. ProCoDA turned this pump on and off via a normal valve control, so long as the pump was already set to a proper flow rate. The system was set to run on Manual setting, as a proper run time had not yet been determined.

The method file was set to control the revolutions per minute (RPM) of the PACl/dye pump and the tap water pumps. This was done using the peristaltic pump ProCoDA file available in the AguaClara server as well as inputs for desired flow rate and tubing size. For the PACl and fluoride pump heads, inputs of $\mathrm{\frac{mL}{rev}}$ and flow rate were needed to calculate RPM since microtubing was used, and for the water pump head, tubing ID and flow rate were needed to calculate RPM. The set points used for the method file included a water pump set point for the water pump RPM and a floc pump set point for the PACl/dye pump RPM.

### States
![Just water](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/waterrules.png)
Figure 7: Screenshot of Just Water State

![Run Experiment](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/Runrules.png)
Figure 8: Screenshot of Run Experiment State
### Set Points

![Setpoints](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/Setpoints.png)
Figure 9: Screenshot of set points in ProCoDA

## Python Code

### Calculations for Water Pump Speed
Calculates RPM of water pump, given a desired upflow velocity in the sedimentation tube.

```python
import math as m
import numpy as np
from aide_design.play import*
#D=diameter of 1 inch sed tube
D=(1)*u.inch
D=D.to(u.m)
#A=area of sed tube
A=np.pi*(D**2)/4
print(A)
#v=velocity of flow through sed tube
v=(0.0015)*(u.m/u.s)

#Q=flowrate through sed tube
Q=(A*v)
print(Q)
Q=Q.to((u.milliliter)/(u.second))
print(Q)

#Manual calculation of RPM
Man_RPM=(Q/((0.8)*(u.milliliter)))
Man_RPM=Man_RPM*(60*(u.second))
print(Man_RPM)

```

### Calculations for Coagulant Pump Speed
Calculates RPM of coagulant pump, given a desired concentration in the system.
Assumes flow rate of coagulant pump is negligible compared to the water pump flow rate.

```python
#Aim for 6.5 mg/L of PAC the lowest according to Github Issues
pump_speed_PACl = 15*(u.rpm)
orange_yellow = 0.019*(u.milliliter/u.revolutions)
oy_flowrate_PACl = orange_yellow.to(u.liter/u.revolutions)*(pump_speed_PACl).to(u.revolutions/u.s)

print('The PACl flow rate is: '+str((oy_flowrate_PACl).to(u.milliliter/u.s))) #Qstock

Q_sys=Q.to((u.liter)/(u.second)) #From Calculations for Water Pump speed and assume oy_flowrate is negligible for now
Q_stock_PACl = oy_flowrate_PACl
C_sys_PACl = 10*(u.mg/u.L) #user input desired concentration of PACl in the system

C_stock_PACl = (Q_sys*C_sys_PACl)/Q_stock_PACl
print('The PACl concentration in the stock is: ' +str(C_stock_PACl))
#M1V1=M2V2 to obtain volume of fluoride stock needed
M_superstock_PACl = (70.28 * (u.g/u.L)).to(u.mg/u.L) #concentration of PACl provided by Cornell water treatment facility
M_stock_PACl = C_stock_PACl
V_stock_PACl = 0.5 * u.L #total volume of the stock (water+fluoride)
V_superstock_PACl = (M_stock_PACl*V_stock_PACl)/M_superstock_PACl
print('The PACl superstock volume in the stock is: ' +str((V_superstock_PACl).to(u.milliliter)))
V_water_PACl = V_stock_PACl-V_superstock_PACl
print('The water volume in the PACl stock is : ' +str((V_water_PACl).to(u.milliliter)))
```

### Fluoride Pump Speed and Stock Concentration
Calculates volumetric flow rate of fluoride pump, given pump speed in RPM.
Calculates concentration of fluoride in system.
Assumes flow rate of fluoride pump is negligible compared to the water pump flow rate.
Uses tube sizing conversions found on [AguaClara Confluence ](https://confluence.cornell.edu/display/AGUACLARA/Auto+Tutorial+for+Peristaltic+Pumps).
<!-- Consider making the section below into a function with variable inputs-->
```python

#Assume Qstock, Qsystem and Csystem

pump_speed = 3*(u.rpm)
#yellow_blue = 0.149*(u.milliliter/u.revolutions)
#yb_flowrate = yellow_blue.to(u.liter/u.revolutions)*(pump_speed).to(u.revolutions/u.s)
orange_yellow = 0.019*(u.milliliter/u.revolutions)
oy_flowrate = orange_yellow.to(u.liter/u.revolutions)*(pump_speed).to(u.revolutions/u.s)

print('The fluoride flow rate is: '+str((oy_flowrate).to(u.milliliter/u.s))) #Qstock

Q_sys=Q.to((u.liter)/(u.second)) #From Calculations for Water Pump speed and assume oy_flowrate is negligible for now
Q_stock = oy_flowrate
C_sys = 3*(u.mg/u.L) #user input desired concentration of F- in the system

C_stock= (Q_sys*C_sys)/Q_stock
print('The fluoride concentration in the stock is: ' +str(C_stock))
#M1V1=M2V2 to obtain volume of fluoride stock needed
M_superstock = 10000 * (u.mg/u.L) #concentration of fluoride provided
M_stock = C_stock
V_stock = 0.5 * u.L #total volume of the stock (water+fluoride)
V_superstock= (M_stock*V_stock)/M_superstock
print('The fluoride volume in the stock is: ' +str((V_superstock).to(u.milliliter)))
V_water=V_stock-V_superstock
print('The water volume in the stock is : ' +str((V_water).to(u.milliliter)))

percent_flow = (oy_flowrate/Q_sys)*100
print('The percent flow rate of fluoride/total flow through system: '+str(percent_flow)+' %.')

total_flowrate = oy_flowrate_PACl + oy_flowrate + Q
print('The total flowrate through the system is: '+str(total_flowrate))
water_flowrate = 0.76 * (u.milliliter/u.s) - (oy_flowrate + oy_flowrate_PACl)
print('The actual water pump flow rate required is: '+str(water_flowrate))

```
### Calculations for Gravity Powered System
<!-- Comment code more! -->
```python
import math as m
import numpy as np
from aide_design.play import*
import aide_design.floc_model as fm
#Q=flowrate of system
Q=.76*(u.milliliter)/(u.second)
Q.to(u.m*u.m*u.m/u.s)
#D=diameter of tubing
D=(1/8)*u.inch
D.to(u.m)
A=np.pi*(D**2)/4
print(A)
#Area given our diameter of tubing
v=(Q/A).to(u.m/u.s)
print(v)

#velocity through our tubing given volumetric flow and area
L=9.43*u.m
T = 298 * u.degK
vis = pc.viscosity_kinematic(T)
print(vis)

#kinematic viscosity given the temperature
Gcoil=206.907*(1/u.s)
g=9.81*(u.meter)/(u.second)/(u.second)
hf=((Gcoil**2)*vis*L/v/g).to(u.m)
print(hf)
R_c = 0.05*u.m
shearG = fm.g_coil(Q,D,R_c,T)
print(shearG)

#Shear gradient in flocculator given curvature and volumetric flow
hfModel=((shearG**2)*vis*L/v/g).to(u.m)
print(hfModel)

#headloss due to the flow through the flocculator
deltah2=((v**2)/2/g+hf).to(u.m)
print(deltah2)

#height difference necessary for the velocity the team wants
Qpacl=.00475*(u.milliliter)/(u.second)
Qpacl.to(u.m*u.m*u.m/u.s)
Dpacl=.0005588*(u.m)

#Use microbore inner diameter of 1/50 inches
Apacl=np.pi*Dpacl*Dpacl/4
print(Apacl)
vpacl=Qpacl/Apacl
print(vpacl)
headP=.05*(u.meter)
Lpacl=headP*g*Dpacl*Dpacl/32/vis/vpacl
Lpacl.to(u.m)
print(Lpacl)
#length of microbore tubing necessary for the given headloss
```


```python
# To convert the document from markdown to pdf
pandoc Fluoride_Summer2018.md -o
Fluoride_Summer_2018_final .pdf
```
