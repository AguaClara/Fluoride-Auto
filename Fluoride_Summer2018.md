# Fluoride, Summer 2018
#### Ching Pang, Kevin Sarmiento, Cheer Tsang
#### July 27, 2018

## Abstract

 Fluoride is a major contaminant in drinking water in many parts of India. The fluoride team's overarching goal is to create low cost, compact, and sustainable solutions to fluoride contamination in drinking water. The summer fluoride subteam aims to continue and expand upon the work of previous fluoride teams by running experiments with both the pump controlled system and the gravity powered system. The goal for the summer is to optimize the amount of coagulant needed to reduce the effluent fluoride concentration to 1$\mathrm{\frac{mg}{L}}$, per the fluoride standard in India and design a easily adjustable gravity powered system. In addition, the team aims to develop a simple user guide for the fluoride probe in order to maximize future teams efficiency.
<!--Use third person for reports, eg. rather than "Our", use "the team" --> <!--Addressed -->
## Introduction

The recent expansion of AguaClara technology to new places around the world like India has uncovered new challenges and prompted new goals for AguaClara. In Honduras, where the majority of AguaClara plants have been constructed, the source of water designated for filtration comes from surface waters such as rivers and lakes. These waters typically have a high amount of particulate matter and as a result also carry biological contaminants. However, in India 85% of the population drinks groundwater extracted from wells and aquifers. Contrast to surface water sources like in Honduras, groundwater contains nearly no particulate matter as many of the particles are naturally filtered out as the water percolates through the soil and rock material. While this natural filtration process is capable of removing particulate matter and reducing microorganisms it also offers the opportunity for minerals and metals to leach into the water. The kinds of minerals that get into the water depend heavily on the types of parent rock material and soils found in the region. India lies on what is known as one of the Fluoride Belts which are expanses of land that are geologically fluoride rich and have a much greater capacity to leach fluoride into the groundwater. According to the World Health Organization one of these belts stretches from Syria through Jordan, Egypt, Libya, Algeria, Sudan, and Kenya while another starts in Turkey and goes through Iraq, Iran, Afghanistan, India, Northern Thailand, and China [(Water-related diseases, 2016)](http://www.who.int/water_sanitation_health/diseases-risks/diseases/fluorosis/en/). India contains about 14% of the total fluoride on the earth's crust, which inevitable leads some of it to leach into the groundwater [(Mondal, Dutta, & Gupta, 2016)](https://doi.org/10.1007/s10653-015-9743-7).

There are a number of public health implications associated with both underconsumption and overconsumption of fluoride. Fluoride is a common additive to municipal water systems in places like the United States where there is little to no fluoride naturally present in the water. Fluoride is added in order to prevent the onset of dental caries. New York City for example adds fluoride to its water supply in order to achieve a concentration of 0.7$\mathrm{\frac{mg}{L}}$ in their effluent supply [(NYC DEP, 2016)](http://www.nyc.gov/html/dep/pdf/wsstate16.pdf). The American Dental Association has set the recommended concentration of fluoride in drinking water at 0.7$\mathrm{\frac{mg}{L}}$ for the prevention of dental cavities [(ADA, 2017)](https://www.ada.org/en/member-center/oral-health-topics/fluoride-topical-and-systemic-supplements). There are however a number of health risks associated with the consumption of fluoride at higher concentrations.

The World Health Organization has set an absolute limit on the concentration of fluoride in drinking water at 1.5$\mathrm{\frac{mg}{L}}$ in order to minimize the negative impacts of elevated fluoride on human health. Dental fluorosis, the mildest condition caused by the consumption of fluoride, can begin with water concentrations above 0.9$\mathrm{\frac{mg}{L}}$. Skeletal fluorosis, a much more serious condition, can begin to develop with fluoride concentrations above 3$\mathrm{\frac{mg}{L}}$. Lastly, At concentrations above 10$\mathrm{\frac{mg}{L}}$ crippling skeletal fluorosis will begins to occur  [(WHO, 2004)](http://www.who.int/water_sanitation_health/dwq/chemicals/fluoride.pdf). The cases of dental fluorosis, the most mild indicator of excessive fluoride, varies across India, but has been shown to range from 13-91 percent depending on the demographic in question and their geographic location [(Arlappa et al., 2013)](http://www.ijrdh.com/files/11.Fluorosis.pdf). While there is no established average for fluoride in Indian groundwater, concentrations in some extreme cases have been measured to be as high as 20$\mathrm{\frac{mg}{L}}$ in some regions but most frequently are below 5$\mathrm{\frac{mg}{L}}$ [(LeChevallier and Au, 2004)](http://www.who.int/water_sanitation_health/publications/9241562552/en/).

The Bureau of Indian Standards have created water quality standards designed to protect the public from the adverse effects of fluoride. They have set the upper limit for fluoride at 1 $\mathrm{\frac{mg}{L}}$ and the permissible limit in the absence of an alternate source at 1.5 $\mathrm{\frac{mg}{L}}$ [(Bureau of Indian Standards, 2012)](http://archive.org/details/gov.in.is.10500.2012). The fluoride team has set their fluoride standards to the standards set by the Bureau of Indian Standards and therefore will be striving to achieve an effluent fluoride concentration of 1 $\mathrm{\frac{mg}{L}}$ or lower. The team will be experimenting with fluoride concentrations up to 20 $\mathrm{\frac{mg}{L}}$ in order to simulate the highest concentrations our systems may encounter out in the field.


## Previous Work

The Spring 2018 team set up a bench experiment using ProCoDA that allowed for precise control of the flow rates of water, fluoride, and coagulant. Polyaluminum chloride (PACl) is the coagulant used in the system. The 2018 team also switched from using a sand filtration system to a flocculation/sedimentation process, which included a tube settler designed by the High Rate Sedimentation team. The sand filtration posed many issues, such as an increase in headloss over time due to the buildup of particles in the filter, which caused clogging. Thus, the flocculation/sedimentation process traditionally used in drinking water treatment was proposed as a possible fluoride removal method.
<!--Replace reactor with sed tank/tube settler.  Consider briefly explaining the justification for the switch #done -->
The team ran several tests with various influent concentrations of fluoride and PACl to determine the optimal PACl dosage to treat a given concentration on influent fluoride. The target effluent fluoride was 1.5 mg/L, based on standards set by the World Health Organization (WHO). At the maximum PACl dosage, the reactor became clogged with a fluidized bed, due to insufficient shear to break up the flocs. The team suggested adding a second reactor to decrease the maximum PACl required. The results have been thus far inconclusive, and the team suggested that the source of error may be a faulty fluoride probe. The team ordered a replacement probe ([Akpan, 2018](https://github.com/AguaClara/fluoride/blob/master/FluorideReportSp18.md)).

In addition, the Spring 2018 fluoride team built a gravity-powered system. The constant head tanks for fluoride and coagulant ensure constant flow through the system. The heights of the constant head tanks were calculated using Bernoulli's equation:

$$ P_1 + \rho g \Delta h_1+ \frac{1}{2}\rho {v_1}^2 = P_2 + \rho g \Delta h_2+ \frac{1}{2}\rho {v_2}^2+ h_f $$

Details on design calculations can be found [here](https://github.com/AguaClara/fluoride/blob/master/Gravity%20Reactor.md). More information can be found in the Spring 2018 [report](https://github.com/AguaClara/fluoride/blob/master/FluorideReportSp18.md).

![gravity_schematic](https://github.com/AguaClara/fluoride/blob/master/fluoride%20report/Gravity%20Powered%20Reactor%20(2).jpg?raw=true)
Figure 1: Schematic for gravity-powered system. The constant head tanks for fluoride and PACl ensure constant flow through the system.

![gravity_reactor](https://github.com/AguaClara/fluoride/blob/master/fluoride%20report/labeledGravSystem.PNG?raw=true)
Figure 2: The fabricated gravity-powered system. The system includes a flocculator and a sedimentation tube.


## Methods
### Experimental Apparatus

The experimental apparatus included pumps, a coiled flocculator, and a sedimentation tube ([Figure 1](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Bench%20setup.png)). Two new sedimentation tubes were fabricated. Fabrication details are listed below, under the Manual section. Water flows into the system through the water pump. Fluoride and coagulant (PACl) are pumped into the system from their respective stock tanks. The pumps are operated by ProCoDA (Process Controller and Data Acquisition), which is a process control software created to automate pump control and generate datalogs ([Weber-Shirk, 2016](https://confluence.cornell.edu/display/AGUACLARA/ProCoDA)). The water, fluoride, and PACl mixture flows into the coiled flocculator. In the flocculator, PACl particles collide with fluoride ions, forming flocs. The mixture flows from the coiled flocculator to the sedimentation tube. Water flows up the sedimentation tube at a rate of 1.5 mm/s. This upflow velocity was used to calculate the necessary flow rate of water through the system. Calculations for the system flow rate can be found [here](https://github.com/AguaClara/fluoride/blob/master/SummerFluorideCalculations.md). Flocs are pumped from the sedimentation tube by a 1 rpm waste pump and exit through the floc weir. The treated water exits the sedimentation tube through the top where it flows to a sampling container. A sample is taken from the sampling container and the fluoride of the effluent water is measured by a fluoride probe.
<!--For your flow rate calculations, you should talk with Hannah about creating a simple function and pushing it to AIDE_design, since you are both using roughly the same calculation #done -->
![bench_setup_drawing](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Bench%20setup.png?raw=true)
Figure 3: A schematic drawing of the bench setup for the fluoride removal system.
![bench_setup](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/Labeled_bench_setup.jpg)
Figure 4: Actual bench setup for the fluoride removal system.
<!--Include a photo of your setup, with each component numbered --> <!--Addressed -->

### Procedure

The stock concentrations for fluoride were prepared to model the actual fluoride concentrations observed in India's groundwater. A range of 20 mg/L to 5 mg/L were tested, since the highest reported fluoride concentration in groundwater was 20 mg/L, while the average amount of fluoride among most regions was 5 mg/L ([Karthikeyan and Lakshanan, 2011](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/Fluoride_book_chapter.pdf)). The goal was to reduce the fluoride influent concentration to 1.0 mg/L, to meet the India fluoride standards for drinking water ([Bhawan and Marg, 2009](https://github.com/AguaClara/fluoride)). In order to achieve the desired system concentrations of fluoride, the stock concentrations were prepared taking into account the flow rate of water through the system.

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
Figure 4: The fluoride probe used to measure effluent fluoride concentration.

The fluoride probe uses an ion-sensitive electrode ([Light, 1975](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/fluoride_paper.pdf)). When the fluoride probe is placed into a solution, the probe outputs a voltage reading. This voltage reading can then be converted to a fluoride concentration by using a calibration curve.

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

###Sample Calculation
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
![calibration_curve](https://github.com/AguaClara/fluoride/blob/master/Summer%202018%20fluoride%20report/calibration_curve.jpg?raw=true)
Figure 5: (add figure of calibration curve after finishing calibration) The linear equation that represents the relationship between voltage and concentration is (). The R-squared value is (). The slope is (), and the y-intercept is ().


## Future Work

In order to make running experiments easier we plan on modifying the gravity powered system further. The goal is to make all the platforms easily adjustable in order to manually change the flow rate of both the water with fluoride and the coagulant. It would be ideal to only use one stock concentration of PACl and change the flow rates in order to achieve the desired concentrations in the system.

## Bibliography
ADA. (2017). Fluoride: Topical and Systemic Supplements. Retrieved from https://www.ada.org/en/member-center/oral-health-topics/fluoride-topical-and-systemic-supplements

Akpan, P. Mehrabyan, T. Sausele, D., Fluoride, Spring 2018. Retriecved from https://github.com/AguaClara/fluoride/blob/master/FluorideReportSp18.md

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
<!--I would refer to this as a tube settler or sed tank, not a reactor, which is ambiguous --> <!--Addressed-->
The sedimentation tube in both the bench system and the gravity powered system had multiple leakages. Therefore, two new tube settlers were fabricated by cutting out 2 sets of PVC pipes for the tube settler (90 cm) and floc weir (40 cm) according to [2017 Fall HRS team final report](https://confluence.cornell.edu/display/AGUACLARA/High+Rate+Sedimentation?preview=/327614520/350974719/high-rate-sedimentation%20(5).pdf).
60 degree bends from the horizontal were created using a welder. Drill bit of 1/2 inch and thread of 1/4 inch were used. Holes were drilled into reactor for floc weir using circle saw and by setting the drill press at 55 degree angle. Floc weir pipe was then welded to the tube settler.
<!--For future fabrication it would be cool to get photographs of the process of building it -->
![sedtank](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/InkedSedtank_LI.jpg)
Figure 5: Reactor fabricated for both the bench system and gravity powered system. THe 1 inch tubing is 90cm in length and the 1/2 inch tubing is 40cm in length.
<!-- Can you add the dimensions of each part of the pipe to the image? -->
### Gravity Powered System
Fixes to the gravity powered system from the [2018 Spring fluoride removal team final report](https://github.com/AguaClara/fluoride/blob/master/FluorideReportSp18.md) were made which included fixing several leaks throughout the apparatus. The newly fabricated reactor was installed to fix the leakages. Valves as shown in figure 4 were added to the exits of the constant head tank and stock tank so that the both tanks can be removed separately for easier refills.

![Valves](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/Valves.jpg)
Figure 4: Valves added at the exits of both stock tank and constant head tank

The height between the sedimentation tube and fluoride constant head tank as shown in figure 5 was adjusted since outflow velocity from the 2018 Spring team could not reach 1.5 mm/s. The constant head tank was lifted with an additional vertical bar added for greater support. Therefore, the distance was increased so that the flow rate measured from the effluent reached 0.76 mL/s, allowing an outflow velocity of 1.5 mm/s.

![Gravity Powered System Adjustment](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/Labelled_bluedye.jpg)
Figure 5: Adjustment to the Gravity Powered System



## Experimental Methods

### Electricity-Powered Fluoride Experiments
The following are improvised based on protocols used for past semesters' experimentation.


#### Protocol for Running Just Water Through the Reactors

1. Open tap water valve and turn off the fluoride pump as to not pump fluoride into the system during backwash <!--I'm confused, when you say tap water valve do you mean the sink or the water line? --> <!-- Addressed. We mean the water line. We are not using the sink at all.-->
2. Close the waste line
3. Turn on Just Water process in ProCoDA and fill system completely with water.
5. Continue to run water until fluoride concentration is less than 0.5 $\mathrm{\frac{mg}{L}}$.
6. Record the initial voltage reading to make sure the initial concentration of fluoride in the sample bottle is about 0 $\mathrm{\frac{mg}{L}}$
<!--Are you cleaning out your turbidimeters with every experiment? --> <!-- We are not using turbidimeter anymore -->
#### Protocol for Start Up and Running of Reactors
1. Fill stock tanks with appropriate concentration of PACl and fluoride, and make sure to have enough stock to run for 24 hours
2. Calculate the flow rates of the PACl and fluoride pumps from the Python file and run the pumps at the appropriate RPM using ProCoDA
3. Run the waste pump at the appropriate RPM as calculated from ProCoDA.
4. Calibrate the fluoride probes and record the initial concentration of fluoride in the sample bottle
5. Empty the bucket at the bottom and make sure it doesn't overflow through the length of the test

#### Experimental Checklist:
##### Before starting test
1. Waste line is opened. (System will explode if this is not open)
2. No leaks anywhere in system
3. Pumps are all turned on and running at the correct RPM (Check ProCoDA)
4. Pumps are all pumping water in the correct direction (in the direction of the flocculator and reactor)
5. The fluoride pump line is closed and fluoride valve is open after running just water through the system
6. Write a text file in ProCoDA saying "Start Test" with appropriate descriptors including fluoride concentration, PACl concentration, upflow velocity,etc. and then change the process to the ON state.
##### During test
7. Recheck everything periodically to ensure it is running how it should be and that there are no water leaks
8. Take a influent and effluent sample every 15 minutes by using the valve after fluoride and before coagulant is added (influent) and after the sedimentation tube (effluent).
##### End of test
8. Change the process to the OFF state.
9. Clean the reactor using the "Cleaning  Procedure" after the experiment is completed.

#### Cleaning Procedure
1. Put a piece of sponge in the tube between the flocculator and PACl insert.
2. Run a high velocity jet through the tube to purge the flocculator.
3. Drain both reactors through the valves at the bottom of the reactors.
4. Flush water through both reactors with water.

#### Fluoride Probe Calibration Procedure
1. Make the stock calibration concentrations of 0.1 $\mathrm{\frac{mg}{L}}$, 0.3 $\mathrm{\frac{mg}{L}}$, 0.5 $\mathrm{\frac{mg}{L}}$, 1 $\mathrm{\frac{mg}{L}}$, 3 $\mathrm{\frac{mg}{L}}$, 5 $\mathrm{\frac{mg}{L}}$, $\mathrm{\frac{mg}{L}}$, 10 $\mathrm{\frac{mg}{L}}$, 15 $\mathrm{\frac{mg}{L}}$,and 20 $\mathrm{\frac{mg}{L}}$ in small bottles. Individually pipette fluoride stocks into all four bottles, do not use serial dilutions.
2. Rinse the fluoride probe with DI water and carefully dab the end of the probe on a Kimwipe. If any sediments from prior experiments remain, rub off with polishing
3. Insert the probe into one of the calibration solutions.
4. Swirl the probe around, then let settle. Record the voltage once it reaches a steady state
5. Make sure to record the voltage at the minimum voltage (the voltage will spike first and eventually reach a steady state voltage before increasing again). <!--Add a photo of what this graph looks like.  How long does it generally take to measure steady state? -->
6. Repeat with the other fluoride concentrations and record the values in Google Docs (labeled "Fluoride Calibration"). ![Summer Fluoride Calibration](https://docs.google.com/spreadsheets/d/1Qdzn8rtu0ubeyHFeoxpHNJPTBkcbFvO21DLpOUB-Flc/edit#gid=0)<!--Add a link to the google doc -->
7. The R squared value, slope, and y-intercept will be updated as the voltages are updated (make sure the R squared value is at least .99 to ensure accurate fluoride calibrations).
8. If R squared value is not 0.99, rinse let settle in standard solution (50% TISAB and 50% DI water), then rinse thoroughly with DI water. Sand with polishing strip, and repeat procedure, gently shaking probe up and down before first calibration measurement.
<!--Add photos! -->
###ProCoDA Method File

ProCoDA is a process control system that was developed by Monroe Weber-Shirk in order to set process parameters through a computerized system. It can be adjusted to different system states that control the system pumps depending on what flow rates are desired. Additionally, ProCoDA collects the data from probes, allowing for compilation of dye concentration data.

To begin the ProCoDA method file, three states were made: ON and OFF and Just Water. In the OFF state, all the valves were closed and no pumps were on. In the ON state, all the pumps were ON and all valves were opened, in the Just Water state, only the water valve was open. ProCoDA turned this pump on and off via a normal valve control, so long as the pump was already set to a proper flow rate. The system was set to run on Manual setting, as a proper run time had not yet been determined.

The method file was set to control the revolutions per minute (RPM) of the PACl/dye pump and the tap water pumps. This was done using the peristaltic pump ProCoDA file available in the AguaClara server as well as inputs for desired flow rate and tubing size. For the PACl and fluoride pump heads, inputs of $\mathrm{\frac{mL}{rev}}$ and flow rate were needed to calculate RPM since microtubing was used, and for the water pump head, tubing ID and flow rate were needed to calculate RPM. The set points used for the method file included a water pump set point for the water pump RPM and a floc pump set point for the PACl/dye pump RPM.

### States
![Just water](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/waterrules.png)
Figure 6: Screenshot of Just Water State

![Run Experiment](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/Runrules.png)
Figure 7: Screenshot of Run Experiment State
### Set Points

![Setpoints](https://raw.githubusercontent.com/AguaClara/fluoride/master/Summer%202018%20fluoride%20report/Setpoints.png)
Figure 6: Screenshot of set points in ProCoDA

## Python Code

### Variables

<!--Comment code more!  Define variables and explain what each section is doing at a higher level of detail! -->
#Calculations for Water Pump speed
Calculates RPM of water pump, given a desired upflow velocity in the sedimentation tube.

```python
import math as m
import numpy as np
from aide_design.play import*

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

```

#Calculations for Coagulant Pump speed
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
M_superstock_PACl = (70.28 * (u.g/u.L)).to(u.mg/u.L) #concentration of fluoride provided
M_stock_PACl = C_stock_PACl
V_stock_PACl = 0.5 * u.L #total volume of the stock (water+fluoride)
V_superstock_PACl = (M_stock_PACl*V_stock_PACl)/M_superstock_PACl
print('The PACl superstock volume in the stock is: ' +str((V_superstock_PACl).to(u.milliliter)))
V_water_PACl = V_stock_PACl-V_superstock_PACl
print('The water volume in the PACl stock is : ' +str((V_water_PACl).to(u.milliliter)))
```

#Fluoride pump speed and stock concentration
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
# Calculations in the report
<!-- Comment code more! -->
```python
import math as m
import numpy as np
from aide_design.play import*
import aide_design.floc_model as fm

Q=.76*(u.milliliter)/(u.second)
Q.to(u.m*u.m*u.m/u.s)
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
pandoc Fluoride_Summer2018.md -o Fluoride_Research_Summer_Report.pdf
```
