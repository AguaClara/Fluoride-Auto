# Fluoride Automated System, Spring 2019
#### Dominic Grasso, Melissa Louie, Desiree Sausele, Emily Spiek
#### March 15, 2019

## Abstract

The Spring 2019 Fluoride Auto subteam aimed to determine the optimal dosage of polyaluminum chloride (PACl) needed to precipitate fluoride ions out of influent water to meet the World Health Organization’s drinking water standard for fluoride concentration (1.5 mg/L). The team accomplished several fabrication tasks, including lengthening the flocculator used by the Fall 2018 subteam and constructing a new sedimentation tube. The team tested the new apparatus with PACl and red dye to visually determine that it worked properly and that aggregated particles (flocs) were exiting the tube through the floc weir. The team then aimed to run experiments with fluoride but experienced difficulty calibrating the fluoride probe. Upon acquiring a new probe in the future, the team will analyze fluoride removal efficiency using the Langmuir Adsorption Model.      

## Introduction
Fluoride, in moderation, can provide a variety of health benefits. It can prevent tooth decay and, over time, strengthen teeth. However, overexposure to fluoride can cause dental fluorosis among other health issues. In India - where AguaClara expects to build new water treatment facilities - 85% of drinking water is sourced from groundwater, but this groundwater often displays excess levels of fluoride due to rocks in aquifers that leach large quantities of fluoride into the water. The prevalence of dental fluorosis - an indicator of excessive fluoride concentrations - differs across India, but has been shown to range from 13-91% depending on the age group in question and the water source supplying the state or municipality [(Arlappa et al., 2013)](http://www.ijrdh.com/files/11.Fluorosis.pdf).

In accordance with AguaClara's mission to create affordable, reliable, and sustainable water treatment solutions, the goal of the Fluoride Auto subteam is to treat groundwater that contains excessive fluoride concentrations. Teams from previous semesters analyzed the efficiency of fluoride removal by passing a coagulant, polyaluminum chloride (PACl), and a solution of fluoride through a sand filter. However, the sand filter was an inefficient removal method because of the buildup of head loss from particles deposited in the sand filter that eventually prevented water from flowing through [(Dao et el., 2015)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride). Thus, instead of using a traditional sand filter, the team researched a similar relationship between PACl and fluoride via a floc blanket reactor. Flocs are aggregates of particles that are created through collision and precipitate out into the water. A floc blanket is a "...fluidized bed of flocs that are maintained in the bottom of an upflow sedimentation tank" [(Weber-Shirk, 2012)](http://cuaguaclara.blogspot.com/2012/08/the-floc-blanket-quest.html). The highly concentrated suspension of flocs in the sedimentation tank filters influent water by trapping incoming flocs, thus reducing the turbidity of effluent water. Once the floc blanket reaches the height of the floc weir tube (which is connected to the side of the sedimentation tube), flocs will begin to overflow into the weir tube while purified water flows out through the top of the reactor. This reactor was modeled after the floc blanket, floc weir, and plate settlers setup in the sedimentation tank of a typical AguaClara water treatment plant (see Figure 1). The team expected that the floc blanket reactor would be able to remove fluoride with a significantly higher efficiency than the sand filter from previous semesters and could run for extended periods of time due to the absence of head loss buildup in the reactor. The flocs in the floc blanket could exit the floc weir while the fluoride in the sand filter would build up and saturate the sand in a short amount of time [(Longo et al., 2016)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride) [(Cheng et al., 2016)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride).

<img
align = "center"
src="https://github.com/AguaClara/Fluoride-Auto/blob/master/Spring%202019/Images/sed%20tube%20diagram.png?raw=true" >

Figure 1: A diagram of the sedimentation tube used by the Spring 2019 subteam

The main goal of the Fluoride Auto subteam was to analyze fluoride removal by researching and constructing Langmuir isotherms. Langmuir isotherms are used to explain adsorption mechanisms. They are based upon the assumptions that there are a fixed number of adsorption sites, and each site can hold one adsorbed molecule. The Spring 2019 team fit a Langmuir isotherm to previous data obtained in Summer 2018 and Fall 2018 by Fluoride subteams. After discovering issues with various data points, the Langmuir isotherm plots were constructed with the removal of some data points. Once the Langmuir isotherm is verified, the information can be applied to other dissolved species removal teams in AguaClara.

The Fall 2018 Fluoride Auto subteam faced the issue of gel formation in their sedimentation tube, which prevented the floc blanket from exiting through the weir. The cause of the gel formation was not entirely known but was theorized to have occurred due to an oversaturation of flocs in the floc blanket. The Spring 2019 team, therefore, reconstructed the sedimentation tube with the weir in a lower position.

In the future, the team will attempt to validate the Langmuir isotherms constructed by teams in previous semesters. The team will also attempt to determine a safe method of disposal for fluoride after it has been removed from the drinking water. This course of action, when determined, will be essential in the implementation of fluoride-removal plants in India.

## Literature Review

#### *Fluoride Limitations and Hazards*

Although small quantities of fluoride in drinking water can be beneficial to human dental health by reducing cavities, over-consumption of fluoride can lead to a number of health concerns, including arthritis, dental fluorosis, bone deformation, ligament calcification [(Roholm, 1937)](http://cof-cof.ca/wp-content/uploads/2012/10/Roholm-Fluorine-Intoxication-A-Clinical-Hygienic-Study-Copenhagen-Denmark-1937.pdf), and even neurotoxic consequences such as reduced cognitive ability [(Choi, 2012)](https://ehp.niehs.nih.gov/doi/full/10.1289/ehp.1104912). According to the National Research Council (NRC), the maximum contaminant level (MCL) of fluoride in drinking water should be 4 $\mathrm{\frac{mg}{L}}$. However, a secondary limit of 2 $\mathrm{\frac{mg}{L}}$ has been established by the EPA to avoid potential cosmetic effects such as tooth and skin discoloration. The World Health Organization (WHO) established a safe upper limit of 1.5 $\mathrm{\frac{mg}{L}}$ to avoid all potential risks of fluoride consumption. Groundwater fluoride levels in India vary from 5 to 23 $\mathrm{\frac{mg}{L}}$, which is well above any established recommended limit and has caused many of the aforementioned health concerns in communities with contaminated water. [(LeChevallier and Au, 2004)](http://www.who.int/water_sanitation_health/publications/9241562552/en/). The Fluoride Auto subteam strives towards the WHO guideline of 1.5 $\mathrm{\frac{mg}{L}}$ of fluoride when designing and experimenting with the floc blanket reactor and manipulating the ratios and concentrations of PACl in the system.

#### *Polyaluminum Chloride (PACl) and Fluoride Removal*
AguaClara water treatment consists of a series of coagulation, flocculation, and clarification. During coagulation, raw water is mixed with a positively charged coagulant (typically an aluminum salt or iron salt), altering or destabilizing any negatively charged particles or dissolved and colloidal contaminants [(EPA, 2016)](https://iaspub.epa.gov/tdb/pages/general/home.do). The destabilized particles then proceed through flocculation, where additional mixing increases the rate of particle collision, forming larger precipitates. Following the formation of flocs, clarification removes the agglomerated particles through sedimentation or other removal processes [(EPA, 2016)](https://iaspub.epa.gov/tdb/pages/general/home.do).

Recently, polymerized forms of aluminum salts have begun to replace standard aluminum salt coagulants [(Ingallinella and Pacini, 2001)](https://www.tandfonline.com/doi/full/10.1080/10934529.2011.598835?scroll=top&needAccess=true). Polyaluminum chloride (PACl), a partially hydrolyzed aluminum salt, is one of the most widely used, as it delivers results similar to those of aluminum sulfate (alum) coupled with a polyelectrolyte [(Ingallinella and Pacini, 2001)](https://www.tandfonline.com/doi/full/10.1080/10934529.2011.598835?scroll=top&needAccess=true). Using PACl instead of alum leads to a reduction in sulfates added to treated water, lower sludge production, reduced odor problems, and higher removal efficiency [(Gebbie, 2001)](http://wioa.org.au/conference_papers/2001/pdf/paper6.pdf). PACl is also less sensitive to temperature changes in its hydrolyzed state and has a broader range of raw water pH in which it is an effective coagulant [(EPA, 2016)](https://iaspub.epa.gov/tdb/pages/general/home.do) [(Yang et al., 2010)](https://www.ncbi.nlm.nih.gov/pubmed/20188465). In particular, for the removal of fluoride, PACl has been found to be the most effective for pH values between 5.2 and 6.2 [(EPA, 2016)](https://iaspub.epa.gov/tdb/pages/general/home.do). Taking these factors into consideration, PACl appears to be the optimal coagulant for fluoride removal, and is thus what the AguaClara Fluoride Auto team currently uses [(Zonoozi et al, 2009)](https://www.ncbi.nlm.nih.gov/pubmed/19381000).

####*Nalgonda Technique for Fluoride Removal*
Current fluoride removal processes need improvement. The Nalgonda technique is a common fluoride removal method that involves a combination of rapid mixing, flocculation, sedimentation, filtration, and disinfection [(Kumbhar and Salkar, 2014)](http://www.ijetae.com/files/Volume4Issue10/IJETAE_1014_22.pdf). Unlike AguaClara treatment, which is a continuous flow process, the Nalgonda technique is a "batch filtration" method, where large quantities of water are treated in buckets. Obtaining safe and treated water for extended periods of time thus requires a series of treatments. Despite the long treatment times, the Nalgonda technique is currently used as a household treatment method in various villages in India. In addition to the restrictions implied by batch treatment, the Nalgonda method requires a high dosage of aluminum sulfate to aggregate with fluoride and precipitate. A study conducted by [(Dahi et al., 1996)](https://wedc-knowledge.lboro.ac.uk/resources/conference/22/Dahi.pdf) suggests that 13 $\mathrm{\frac{g}{L}}$ alum (1.2 $\mathrm{\frac{g}{L}}$ as Al) is needed for the Nalgonda method to effectively treat fluoride levels between 9 and 13 $\mathrm{\frac{mg}{L}}$. Despite the high concentrations of coagulant, the fluoride residual in the test is still unable to meet the WHO safety guidelines of 1.5 $\mathrm{\frac{mg}{L}}$ of fluoride. The high dose of aluminum sulfate also leaves high sulfate residuals in the water, which causes taste and odor issues [(Bailey and Fawell, 2004)](http://apps.who.int/iris/handle/10665/43514). In regards to other filtration methods, a study by Inganiella achieved 33.3% removal of fluoride using a combination of a gravel pre-filter and a rapid sand filter to capture granules of fluoride, PACl, NaClO and $SO_4H_2$ [(Ingallinella and Pacini, 2001)](https://www.tandfonline.com/doi/full/10.1080/10934529.2011.598835?scroll=top&needAccess=true). Clearly, this method is not effective enough to produce safe drinking water.

#### *Floc Blankets*
Floc blankets develop when vertical flow sedimentation tanks form a fluidized bed of particles. An example is shown in Figure 2. A floc blanket then facilitates particle removal by “increasing particle-particle interactions that lead to flocculation and filtration occurring in the floc blanket” [(Hurst, 2010)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.849.6127&rep=rep1&type=pdf).

<div style = "text-align:center">
<img
align = "center"
src="https://github.com/AguaClara/Fluoride-Auto/blob/master/Summer%202018/fluoride%20report/Flocs_in_Reactor.jpg" height=400, width=300>

Figure 2: Floc blanket forming in the reactor

</div>

The process of forming flocs requires both the precipitation of aluminum hydroxide from the coagulant and the contact with colloidal particles present in raw water [(Hurst, 2010)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.849.6127&rep=rep1&type=pdf). Once the combination of precipitation and mixing forms small particles, these new flocs collide to form larger, more porous flocs that can then be used for clarification [(Hurst, 2010)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.849.6127&rep=rep1&type=pdf).

This floc blanket clarification is considered hindered settling, which is a form of sedimentation [(Gregory et al., 1996)](https://link.springer.com/chapter/10.1007%2F978-3-642-61196-4_2). Sedimentation processes are characterized by the removal of suspended particles, e.g. flocs, sand, and clay, from water. Removal is possible due to the differences in density between water and the suspended particles, but it is also dependent on the size of the suspended particles, water temperature, turbulence, stability of flow, bottom scour, and flocculation [(Sun, 2004)](http://onlinelibrary.wiley.com/doi/10.1002/0471623571.ch11/summary). Floc blanket clarification, however, is primarily driven by upflow velocity of the water and by floc concentration, while the other parameters show a weaker correlation with the creation of the floc blanket. [(Gregory et al., 1996)](https://link.springer.com/chapter/10.1007%2F978-3-642-61196-4_2). The relationship between upflow velocity, concentration, and water quality can be combined into the mass rate of settling, which is equal to the product of upflow velocity and concentration. Within a range of mass fluxes, a distinct interface is established between clear water and the floc blanket, and thus one can deduce appropriate values of velocity and floc concentration.  At concentrations above the ideal mass flux range, the aggregation of flocs becomes thick enough that compression settling occurs- an event in which over a quarter of the volume of the coagulant will enter the floc blanket within an hour. At concentrations below that appropriate range, flocs are not inhibited by other particles and a suspension with different settling velocities is formed [(Gregory et al., 1996)](https://link.springer.com/chapter/10.1007%2F978-3-642-61196-4_2).
Examples of floc blanket clarification are shown throughout the world as further proof of its potential in water purification. In Taiwan, a process of pre-sedimentation, floc blanket clarification, and sand filtration is used to reduce 100 NTU water down to potable levels [(Lin et al., 2004)](https://ascelibrary-org.proxy.library.cornell.edu/doi/abs/10.1061/(ASCE)0733-9372(2004)130:12(1481)). Floc blankets have also been used extensively to purify water of algae, protozoa, and specific virus strains [(LeChavallier and Au, 2004)](http://www.who.int/water_sanitation_health/publications/9241562552/en/). Therefore, it is believed that the adaptability of this method in conjunction with the use of PACl would allow for effective fluoride removal.

## Previous Works
Prior to the Spring 2016 semester, the team used a sand filter system that was inexpensive and efficient in removing fluoride. However, the main issue with the sand filter was that it became saturated with PACl and fluoride within several hours, thus building up head loss and rendering the sand filter inadequate at removing fluoride. Consequently, the system required backwashing every few hours, which is inefficient.  In order to address the inefficiencies of the sand filter system, the team fabricated a new single floc blanket reactor [(Longo, 2016)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride) that mirrored that of the floc blanket and plate settlers present in the then-current Aguaclara plants. The team also implemented a new setup that included stock tanks, a reactor, a turbidimeter, a flocculator, and stock and waste pumps, which was consistent with previous research regarding quantity of coagulant added and head loss accumulation [(Dao, 2015)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride).

The Spring 2016 team then developed a MathCad file to calculate flow rates of pumps from a given set of parameters including upflow velocity, tubing diameters, and reactor concentrations. The team also created a ProCoDA method file to turn the flow rates into RPMs for the pumps so that the process of changing PACl and fluoride concentrations within the reactor was more user-friendly. The Spring 2019 Team converted the MathCad file to Python code.

The Fall 2016 team fabricated a new bottom geometry insert within the sedimentation tube to prevent flocs accumulating and clogging the bottom of the tube. The newly designed geometry incorporated a smooth sloped bottom, which allowed for gradual flow expansion and recirculation of flocs at the bottom of the tube.

The team also determined the minimum length of the reactor needed to save resources and space. A shorter reactor, with a height of 5 cm below the weir, was tested with concentrations of 25 $\mathrm{\frac{mg}{L}}$, 50 $\mathrm{\frac{mg}{L}}$, and 100 $\mathrm{\frac{mg}{L}}$ of dye. Although the floc blankets reached a short term steady state height of around 20-30 cm, in the long term the flocs built up and traveled through the tube settler to the turbidimeter, indicating a failure in the reactor. This observation suggested that there was some minimum height that a floc blanket would reach, and the team concluded that a shorter reactor system was not feasible [(Longo, 2016)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride).

In Summer 2017, the fluoride team repeated tests from the previous semester to determine whether the improvements made by the second reactor in series were significant enough to warrant implementation on a larger scale. The Summer 2017 team stopped adding clay to the system and focused on the goal of determining a PACl concentration that would optimize fluoride removal rates [(Longo, 2017)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride), which is the main objective of the team. Initial tests indicated reactor failure within 10 hours due to sludge buildup regardless of PACl concentration, so the team switched to using a new reactor designed by the Summer 2017 High Rate Sedimentation team. This new reactor increased the time to failure and allowed for higher upflow velocities. After running various tests, the team determined that an upflow velocity of 1.5 $\mathrm{\frac{mm}{s}}$ was the best way to reduce sludge buildup. The team then ran experiments to examine the effect of higher PACl concentrations on removal rates. Data collected from these experiments was used to create an adsorption model that could calculate the necessary PACl dosage for a desired effluent fluoride concentration.

After creating the adsorption model, the team observed a significant difference in the fluoride probe readings for tap water versus the readings in deionized water. The findings suggested that the amount of fluoride ions in tap water is actually higher than the readings from the fluoride probe state. Therefore, the team deemed the adsorption model to be inaccurate and planned to revise it, taking this discrepancy into consideration.

In the Spring 2018 semester, experiments were conducted with a new fluoride probe, which measured the effluent concentrations of fluoride after treatment with different concentrations of PACl. When a new probe was used, the difference in voltage readings between tap and DI water turned out to be negligible; therefore, it was concluded that the discrepancy from the previous semester may have been caused by a probe issue. The results of the Spring 2018 experiments for removal of fluoride using PACl are summarized in Figure 3.

<div style = "text-align:center">
<img
align = "center"
src="https://github.com/AguaClara/fluoride/blob/master/Summer%202018/fluoride%20report/Results.png?raw=true>

Figure 3: A summary of the experimental results of final fluoride concentrations based on varied concentrations of initial and PACl concentrations.

<div style = "text-align:left">

In Summer 2018, the team ran experiments to measure the effluent concentrations of fluoride for different concentrations of PACl to construct an adsorption model, which could be used to predict the PACl dosage required for a desired effluent fluoride concentration and would generate an adsorption density value for the mass of fluoride adsorbed (W). The WHO standard for fluoride levels is 1.5 $\mathrm{\frac{mg}{L}}$, which is the desired effluent fluoride concentration. Therefore, the model would calculate a range of uptake values that would result in the target effluent concentration. In addition, the model would provide a way to calculate the PACl dosage required to treat an initial fluoride concentration given a range of W values (equation seen below).

$W = \frac{C_{\text{fluoride influent}}-C_{\text{fluoride effluent}}}{C_{PACl}}$

The findings of the Summer 2018 team showed that the reactor would clog due to insufficient shear to break down the PACl flocs, which then caused the bed to fluidize. This result indicates that, for an excessive PACl dosage, a second reactor would be necessary to decrease the maximum concentration of PACl needed to run the system.

However, the Summer 2018 team found that results were inconclusive. For example, influent concentrations of 10 $\mathrm{\frac{mg}{L}}$ and 5 $\mathrm{\frac{mg}{L}}$ of fluoride resulted in the same fluoride effluent concentration of around 3 $\mathrm{\frac{mg}{L}}$ for 12.5 $\mathrm{\frac{mg}{L}}$ of PACl and around 2 $\mathrm{\frac{mg}{L}}$ for 25 $\mathrm{\frac{mg}{L}}$ PACl. It is unlikely that the same dosage of PACl would result in the same effluent fluoride concentration for fluoride inlet concentrations that differ as substantially as by a factor of 2. Therefore, the experiment should be repeated with a more accurate probe before any definitive conclusions can be drawn.

The team then began using the probe that had been ordered in May 2018 for experiments that used the isotherm developed by the Spring 2018 team to change the coagulant dosing. The experiments showed that a 6.25 mg/L dosing of coagulant did not create a floc blanket. As a result, the coagulant dosing used in subsequent experiments ranged from 10 mg/L to 50 mg/L with the influent fluoride concentration ranging from 3 mg/L to 20 mg/L. The team also identified that the influent fluoride concentration did not match the ideal concentration set by the flow rate and stock tank concentration. Therefore, the team began to take manual readings of the influent fluoride before it reached the flocculator to compare with the effluent fluoride reading. These manual readings were used for the Langmuir isotherm derivation in the Fall of 2018.

The Fall 2018 team created a longer reactor due to a low upflow velocity, in accordance with the findings of the Fall 2016 team regarding reactor length. The main goal of the Fall 2018 team was to analyze the Fall 2017 and Summer 2018 Langmuir isotherm that modeled the adsorption of fluoride to PACl. The team used the experimental data from the two previous teams to graph a nonlinear regression to compare the experimental results to the theoretical Langmuir isotherm. The analysis demonstrated that the data closely fit the adsorption model, especially at low concentrations of fluoride. The team also calculated a coefficient of determination of 0.82, indicating that a high percentage of variability in the uptake occurs because of the variability in concentration. While more data is still necessary to confirm the Langmuir isotherm, the team concluded that the model so far is sufficient to predict required PACl concentrations based on fluoride concentrations.

The Fall 2018 team then implemented a new bottom geometry into the reactor system to reduce variability. This new bottom geometry was designed with the intent of guiding flocs to flow parallel to each other and prevent them from colliding and accumulating. However, when the new design was implemented, the formation of a super saturated solution and, subsequently, gel occurred. The first experiment in which gel appeared in the reactor was with a concentration of 40 mg/L PACl and 10 mg/L fluoride. The team hypothesized that either the concentration of PACl was too high or the ratio of fluoride to PACl was too high. Previous experiments were run with up to 50 mg/L PACl concentration without gel formation. Additionally, an aluminum fluoride complex may have formed and repelled other aluminum particles within the solution. While past teams have conducted experiments at higher fluoride concentrations, few experiments were conducted at concentrations of 10 mg/L or higher. The second theory is consistent with this semester's experiments in that the inclusion of the bottom geometry increased gel formation.

In order to more clearly observe the gel formation, the team injected red dye into the sedimentation tube with the PACl. Using this method, the team concluded that gel first formed in the floc hopper, or floc weir, and accumulated until it reached the top of the reactor because of the flow of dye throughout the reactor. The gel only dissociated within the reactor with an upflow velocity of 8 mm/s. The gel within the floc weir was more difficult to remove because it was controlled by a single speed pump.

Further experimentation was conducted using the red dye to produce more visible flocs. The first experiment, which was run with 20 mg/L PACl, showed formation of flocs and later aggregation of the flocs into a gel at the entrance to the floc weir. The team hypothesized that the protrusion of the floc weir into the sedimentation tube provided a surface for flocs to accumulate and form gel. A new sedimentation tube was fabricated to test the hypothesis, and the red dye experiment was replicated in the new tube. The experiment resulted in gel formation, however, flocs entered the floc weir without aggregation at the entrance as observed in the previous reactor. The team hypothesized that gel formed when the flocs that were above the floc weir descended down the sedimentation tube and collided with other flocs, which created a super saturated solution necessary for a gel.

The team continued to run tests at low concentrations of PACl, or a maximum of 20 mg/L, and high concentrations of red dye. However, each experiment gelled, and thus, produced no useful data for further validating a Langmuir adsorption model.


## Methods
### Experimental Apparatus

#### Schematic

<div style = "text-align:center">
  <img src="https://github.com/AguaClara/Fluoride-Auto/blob/master/Spring%202019/Images/fluoride%20spring%2019%20new%20apparatus.jpg?raw=true" >
Figure 4: A schematic drawing of the Spring 2019 Subteam apparatus
<div style = "text-align:left">

</div>

<div style = "text-align:center">
  <img src="https://github.com/AguaClara/Fluoride-Auto/blob/master/Spring%202019/Images/fluoride%20apparatus%20with%20filter%20(2).jpg?raw=true">
Figure 5: The bench setup for the Spring 2019 Subteam
<div style = "text-align:left">

#### Process Flow Through Reactor
1. Fluoride was pumped from the Fluoride stock tank and mixed with tap water.
2. PACl was pumped from the Coagulant stock tank and mixed with the diluted fluoride stream.
3. The mixture was sent to the flocculator to form flocs.
4. The mixture flowed into the sedimentation tube.
5. Flocs built up a floc blanket and exited out through the floc weir.
6. The effluent stream flowed out the top of the reactor. The turbidimeter measured the stream turbidity.
7. The stream flowed through the effluent filter to break up large flocs.
8. The fluoride sensor was immersed in the effluent reactor stream to measure the effluent fluoride concentration.
9. The effluent stream flowed into the sink.
  1. The floc weir effluent was pumped to the waste line by a waste pump.

#### Materials
- One 600 RPM pump, two 100 RPM pumps, and one 1 RPM pump
- Transparent 2.54 cm (1") PVC piping
- Flexible and hard 0.635 cm (1/4") tubing and Microbore tubing
- One Turbidimeter
- 1,000 ppm Polyaluminum Chloride (PACl) stock solution
- 1,000 ppm Fluoride stock Solution
- Connectors and buckets for stock tanks
- Two stir plates with stir bars for the stock solutions
- One Fluoride Probe (Cole-Parmer, Catalog No. UX-27502-19)
- One 47 mm In-Line Filter Holder (Pall Corporation)

#### Apparatus Changes
The Spring 2019 team made various changes to the apparatus from the one used by the Fall 2018 team. The fabrication details are outlined in the manual.
- Flocculator: The flocculator was lengthened to account for the desired amount of head loss. This also increased the retention time which allowed for better floc formation. See [Flocculator](flocculator) for fabrication details.
- Sedimentation Tube: The shape of the reactor tube was reevaluated from what was used in previous semesters. The floc weir was moved from being on the right side of the tube and above the bend to being on the left side of the tube and below the bend. The goal was to have the reactor more closely mimic the sedimentation tanks in AguaClara plants in addition to preventing gel formation within the reactor. The team hoped to mitigate the issue of gel formation by moving the floc weir lower down the tube to allow the floc blanket overflow out of the reactor before gel could form. See [Sedimentation Tube](#sedimentation-tube) for fabrication details.
- Floc filter: The team placed a wire mesh screen between the two plates of a 47 mm In-Line Filter Holder. This filter holder was attached at one end to the effluent tube from the turbidimeter and the influent tube to the bottle where the fluoride probe was. Additionally, a mesh screen with a larger hole was placed over the effluent opening of the sedimentation tube. See [Mesh Filters](#mesh-filters) for fabrication details.
- Bottom geometry: The Fall 2018 team encountered sedimentation tube failure due to gelling from the old bottom geometry. In the middle of the Spring 2019 semester, the team received a new bottom geometry. However, the inlet to the sedimentation tube through this new bottom geometry was too small, which increased the upflow velocity at the bottom of the tube, broke up flocs, and prevented the formation of a floc blanket. The team received a new bottom geometry at the end of the semester (see Figure 6), which is to be implemented in the next semester.

<div style = "text-align:center">
<img src = "https://github.com/AguaClara/Fluoride-Auto/blob/master/Spring%202019/Images/BotGeo%20Drawing.jpg?raw=true">
Figure 6: The newly designed bottom geometry insert
<div style = "text-align:left">

### Procedure
The team used ProCoDA to run the experiments and collect fluoride probe and turbidimeter data. Refer to the manual for more information on the Fluoride Auto ProCoDA method file.

#### Creating the Fluoride Calibration Curve
Before running an experiment, a standard curve was made for the fluoride probe. The team first prepared stock solutions of known fluoride concentrations (1 $\frac{mg}{L}$, 5 $\frac{mg}{L}$, and 10 $\frac{mg}{L}$). Then, through ProCoDA, the voltages of each solution were measured using the fluoride probe. These values were entered into an Excel spreadsheet to create a standard curve as shown in Figure 7. This allowed the team to determine the fluoride concentration in the effluent stream.

<div style = "text-align:center">
<img
align = "center"
src="https://github.com/AguaClara/Fluoride-Auto/blob/master/Spring%202019/Images/std_curve.PNG?raw=true" >
<div style = "text-align:center">
Figure 7: Excel sheet used to calibrate the probe and create a standard curve

<div style = "text-align:left">

#### Running an Experiment
Before running the pumps, the valves for the influent and effluent water lines were opened. In ProCoDA, the state was manually changed to "Just Water," which allowed the sedimentation tube to fill up. This process took about five minutes, during which the team plugged in the 1 RPM waste pump and secured the probe in the fluoride sensor bottle (see Figure 5). After the sedimentation tube filled up completely, the state was switched to "Run Experiment," which started the PACl pump. Because ProCoDA can only control two pumps at once, the fluoride pump was turned on manually. Due to the nature of the team's experiments, the flow rates for the PACl and fluoride pumps varied depending on what concentrations the team was analyzing.

The experiments were run for two hours after which the state was switched back to "Just Water" to clear out the sedimentation tube. The team then turned off all the pumps and closed the influent and effluent water valves, concluding the experiment.

## Results and Analysis
The team ran an experiment to test if the fluoride probe was as accurate at sensing fluoride flocs as it was at detecting ionic fluoride. See [Fluoride Probe Accuracy Test](#fluoride-probe-accuracy-test) for experimental design used.

<div style = "text-align:center">
<img
align = "center"
src="https://github.com/AguaClara/Fluoride-Auto/blob/master/Spring%202019/Images/Probe%20Test.39.24%20PM.png?raw=true" >

Figure 8: Table showing the fluoride concentrations of the effluent directly after collection and after filtering through a mesh screen.

<div style = "text-align:left">

<div style = "text-align:center">
<img
align = "center"
src="https://github.com/AguaClara/Fluoride-Auto/blob/master/Spring%202019/Images/Screen%20Shot%202019-04-11%20at%209.39.41%20PM.png?raw=true" >

Figure 9: Table showing fluoride concentrations of the effluent directly after collection, after shaking/mixing, and after filtering through a mesh screen.

<div style = "text-align:left">

The results, outlined in Figure 8 and 9 above, show a consistent increase in detected fluoride after filtering. The only exception is the first sample, which shows a decrease in the detected concentration after filtering. This first trial used the effluent from cleaning out the sedimentation tube, where the floc blanket had formed a gel from a previous experiment. The team speculated that, in this case, the flocs present in the effluent sample were large enough to be effectively filtered out by the mesh, causing the detected concentration of the fluoride to decrease after filtering. However, since all the other samples showed an increase in detected fluoride concentration, the team believed that the flocs in all samples besides Sample 1 were smaller, and were possibly broken up more by the mesh rather than filtered out due to their size. These smaller flocs were then able to pass through the holes in the mesh.

Both Table 8 and Table 9 show an increase in detected fluoride concentration after filtering, but Table 9 also shows an increase in the concentration after shaking/mixing. Thus, the team believed that shaking the samples also helped break up the flocs into a form of fluoride that the probe was able to sense.

The team also ran two experiments this semester, with different ratios of PACl to fluoride. The team was able to plot these two experiments on the Langmuir Isotherm model developed by the Fall 2018 Team, as seen in Figure 10. The coefficient of determination between the experimental and theoretical trend lines is 0.87.

<div style = "text-align:center">
<img
align = "center"
src="https://github.com/AguaClara/Fluoride-Auto/blob/master/Spring%202019/Langmuir%20Isotherm%20Data/isotherm.png?raw=true" >

Figure 10: Langmuir Adsorption Isotherm showing theoretical vs. experimental trends.

<div style = "text-align:left">


## Conclusions
The Spring 2019 team's two experiments show results that closely match the data from the previous semesters, which confirms that the new sedimentation tube design is capable of removing flocs from an influent water stream in a similar manner to the previous sedimentation tube design, despite the difference in the placement of the floc weir.

Following the fluoride probe test, the team concluded that, when fluoride is in the form of flocs, the concentration detected by the probe is lower than the actual total concentration of fluoride. The team found that both shaking and filtering the effluent samples were effective ways to increase the amount of fluoride that the probes could sense, thus providing a more accurate reading of the effluent fluoride concentration.

The results of the fluoride probe test, which indicated that flocs were broken up by filtration through mesh, also suggests that the bonds between flocs are weaker than covalent bonds. Thus, the Langmuir isotherm, which is valid for covalently bonded molecules, may not work for modeling the bonding of PACl to fluoride.

## Future Work
The team's immediate plan will be to calibrate the newest probe and ensure that it is working and usable. The team will then continue to replicate and analyze the fluoride experiment that was first run during the Fall 2017 and Summer 2018 semesters in order to verify data from the previous teams. The new data will be plotted against the theoretical Langmuir isotherm to determine whether the model can be reliably used to optimize PACl concentrations for desired effluent fluoride concentrations.

Additionally, during several of the experiments, the team observed that the bottom geometry of the sedimentation tube was too far down within the tube and obscured the bottom of the floc blanket. Thus, once the team receives the new bottom geometry that is currently being designed, the new bottom will be implemented in a raised position in order to make it possible to see the initial formation of the floc blanket.

In the Summer 2018 semester and other previous semesters, the Fluoride Auto team used an upflow velocity of 1.5 mm/s. However, the current team decided to run an experiment with an upflow velocity of 1.0 mm/s, which is consistent with the value used in AguaClara plants in the field. Both the Summer 2018 team and the current team encountered the formation of gel in the sedimentation tube and subsequent failure of the apparatus with the lower upflow velocity. Thus, in the next semester, the team will test different upflow velocities between 1 and 2 mm/s to determine an optimal velocity. The upflow velocity should be low enough to allow for the formation of a proper floc blanket but high enough to prevent gelling in the sedimentation tube.

In light of the results of the experiment in which the team filtered the effluent and found flocs were broken up by filtration, the team is considering finding a different model based on ionic rather than covalent bonds between the fluoride and PACl. However, if the Langmuir isotherm ends up being a fitting model for the data, a new model may not be necessary.

The team will eventually design and test a horizontal reactor in which influent water will enter through one end of the sedimentation tube and the flocs will exit through a vertical floc weir in the middle of the reactor.

Finally, the team will research methods of treating and disposing of the effluent waste, which will consist of fluoride and possibly arsenic, which may also be present in the untreated groundwater.

## Bibliography
Arlappa, N., Aatif Qureshi, I., and Srinivas, R. (2013). Fluorosis in India: an overview. Int J Res Dev
Health, 1(2).

Bailey, K. and Fawell, J. (2004). Fluoride in Drinking-water.

Cheng, M., Longo, A., and Vidal, B. (2016). Fluoride, Fall 2016.

Dahi, E., Mtalo, F., Njau, B., and Bregnhj, H. (1996). Defluoridation using the Nalgonda Technique in
Tanzania. In Reaching the Unreached: Challenges for the 21st Century, New Delhi, India.

Dao, K., Desai, P., and Longo, A. (2015). Fluoride, Fall 2015.

Dokko, J. and Espada Fraile, J. (2016). Countercurrent Stacked Floc Blanket Reactor, Fall 2016.

EPA (2016). Water Treatability Database.

Gebbie, P. (2001). Using Polyaluminum Coagulants in Water Treatment.

Golob, V., Vinder, A., and Simoniˇc, M. (2005). Efficiency of the coagulation/flocculation method for
the treatment of dyebath effluents. Dyes and pigments, 67(2):93–97.

Gregory, R., Head, R. J. M., and Graham, N. J. D. (1996). The Relevance of Blanket Solids Concentration
in Understanding the Performance of Floc Blanket Clarifiers in Water Treatment. Chemical Water
and Wastewater Treament, IV.

Hurst, M. W. (2010). Evaluation of Parameters Affecting Steady-State Floc Blanket Performance. Degree
of Master of Science, Cornell University, Ithaca, New York.

Ingallinella, A. M. and Pacini, V. A. (2001). Simultaneous removal of arsenic and fluoride from groundwater
by coagulation-adsorption with polyaluminum chloride. Journal of Environmental Science and
Health, Part A.

Kokko, J. P. and Rector, F. C. (1972). Countercurrent multiplication system without active transport
in inner medulla. Kidney international, 2(4):214–223.

Kumbhar, V. S. and Salkar, V. D. (2014). Use of PAC as a Substitute for Alum in Nalgonda Technique.
International Journal of Emerging Technology and Advanced Engineering, 4(10).

LeChevallier, M. W. and Au, K.-K. (2004). Water Treatment and Pathogen Control.

Lin, W., Chen, L. C., Chung, H. Y., Wang, C. C., Wu, R. M., Lee, D. J., Huang, C., Juang, R. S.,
Peng, X. F., and Chang, H.-L. (2004). Treating High Turbidity Water Using Full-Scale Floc Blanket
Clarifiers. Journal of Environmental Engineering, 130(12):1481–1487.

Longo, A., Desai, P., and Dao, K. (2016). Fluoride, Spring 2016.

Longo, A., Zhang, V., and Cheng, M. (2017). Fluoride, Fall 2017

NJ Department of Health (2010). Sodium Fluoride.

Roholm, K. (1937). Fluorine Intoxication: A Clinical-Hygienic Study. Copenhagen, Denmark.

Sun, S. F. (2004). Sedimentation. In Physical Chemistry of Macromolecules: Basic Principles and Issues,
Second Edition, pages 243–266. John Wiley & Sons, Inc.

Weber-Shirk, M. (2012, August 05). The Floc Blanket Quest. Retrieved March 14, 2019, from http://cuaguaclara.blogspot.com/2012/08/the-floc-blanket-quest.html

Yang, Z. L., Gao, B. Y., Yue, Q. Y., and Wang, Y. (2010). Effect of pH on the coagulation performance
of Al-based coagulants and residual aluminum speciation during the treatment of humic acid–kaolin
synthetic water. Journal of Hazardous Materials, 178(1):596–603.

Zonoozi, M. H., Moghaddam, M. A., and Arami, M. (2009). Coagulation/flocculation of dye-containing
solutions using polyaluminium chloride and alum. water science and technology, 59(7):1343–1351.

# Manual
This manual provides information on fabricating key components of the team's experimental apparatus along with more detailed information on running an experiment.

## Fabrication Details

### Flocculator
To assemble the flocculator, the team wrapped 46 feet of flexible and hard tubing around a tube with a radius of 4.25 cm. The inner diameter of the tubing used was 0.125 inches. One end of the flocculator was attached to the influent water tubing while the other end was attached to the bottom of the sedimentation tube.

### Sedimentation tube
The team created a new reactor that reverts to a design used by the Fall 2016 through Fall 2017 teams, which has a floc weir protruding from the sedimentation tube below the bend rather than above it. The goal of using this design was to minimize gel formation, which was seen around the bend and mouth of the floc weir in the Fall 2018 semester, and to more closely mimic the actual AguaClara plants in the field. The PVC was heated proximate to the bend point in order to create as smooth of a bend as possible; the floc weir was subsequently welded to the side of the reactor.

<div style = "text-align:center">
<img src="https://github.com/AguaClara/Fluoride-Auto/blob/master/Spring%202019/Images/sedimentation%20tube.JPEG?raw=true" height=500 width=350>

Figure 11: The reactor used by the Spring 2019 subteam
<div style = "text-align:left">

### Mesh filters
The team cut a hole into a piece of mesh and placed the mesh over the effluent opening of the sedimentation tube. Additionally, the team placed a mesh screen in a 47 mm In-Line Filter Holder and added the Filter Holder to the apparatus between the turbidimeter and the bottle with the fluoride probe. The idea behind this addition was to break up fluoride flocs that had exited the sedimentation, since the team determined that the fluoride probe was inaccurate at detecting fluoride in the form of flocs. The mesh is small enough to act as a constriction that will break up flocs but not small enough to filter out the flocs.

## Experimental Methods
#### Protocol for Running Just Water Through the Reactors

1. Open tap water valve and close the fluoride valve as to not pump fluoride into the system during backwash
2. Close the waste line
3. Turn on Just Water process in ProCoDA and fill system completely with water.
4. Make sure the sample bottle with the fluoride probe does not overflow from the high flow rate of the water
5. Continue to run water until turbidimeter reads less than 0.5 NTU and fluoride concentration is less than 0.5 $\mathrm{\frac{mg}{L}}$.
6. Record the initial voltage reading to make sure the initial concentration of fluoride in the sample bottle is about 0 $\mathrm{\frac{mg}{L}}$

#### Protocol for Start Up and Running of Reactors
1. Fill stock tanks with appropriate concentration of PACl, fluoride, and clay and make sure to have enough stock to run for 24
hours
2. Calculate the flow rates of the PACl and fluoride pumps from the MathCAD file and run the pumps at the appropriate RPM using ProCoDA
3. Run the waste pump at the appropriate RPM as calculated from ProCoDA.
4. Calibrate the fluoride probes and record the initial concentration of fluoride in the sample bottle
5. Empty the bucket at the bottom and make sure it doesn't overflow through the length of the test

#### Experimental Checklist:
##### Before starting test
1. Waste line is open (System will explode if this is not open)
2. Ensure there are no leaks anywhere in system
3. Pumps are all turned on and running at the correct RPM (Check ProCoDA)
4. Pumps are all pumping water in the correct direction (in the direction of the flocculator and reactor)
5. The fluoride pump line is closed and fluoride valve is open after running just water through the system
6. Write a text file in ProCoDA saying "Start Test" with appropriate descriptors including fluoride concentration, PACl concentration, upflow velocity,etc. and then change the process to the ON state.
##### During test
7. Recheck everything periodically to ensure it is running how it should be and that there are no water leaks
##### End of test
8. Change the process to the OFF state.
9. Clean the reactor using the "Cleaning  Procedure" after the experiment is completed.

#### Cleaning Procedure
1. Put a piece of sponge in the tube between the flocculator and PACl insert.
2. Run a high velocity jet through the tube to purge the flocculator of excess clay buildup.
3. Drain both reactors through the valves at the bottom of the reactors.
4. Flush water through both reactors until no clay remains in the system.
5. If there is not a noticeable amount of buildup, (a) and (b) can be skipped.

#### Fluoride Probe Calibration Procedure
1. Make the stock calibration concentrations of 1 $\mathrm{\frac{mg}{L}}$, 5 $\mathrm{\frac{mg}{L}}$, and 10 $\mathrm{\frac{mg}{L}}$ in small bottles. Individually pipette fluoride stocks into all four bottles, do not use serial dilutions.
2. Rinse the fluoride probe with DI water and carefully dab the end of the probe on a Kimwipe. If any sediments from prior experiments remain, rub off with polishing
3. Insert the probe into one of the calibration solutions.
4. Swirl the probe around, then let settle. Record the voltage once it reaches a steady state
5. Make sure to record the voltage at the minimum voltage (the voltage will spike first and eventually reach a steady state voltage before increasing again).
6. Repeat with the other fluoride concentrations and record the values in Google Docs (labeled "Fluoride Calibration").
7. The R squared value, slope, and y-intercept will be updated as the voltages are updated (make sure the R squared value is at least .99 to ensure accurate fluoride calibrations).
8. If R squared value is not 0.99, rinse let settle in TSIAB solution for 5 minutes, then rinse thoroughly with DI water. Sand with polishing strip, and repeat procedure, gently shaking probe up and down before first calibration measurement.

#### Fluoride Probe Accuracy Test
1. Run an experiment with PaCl and Fluoride. The exact concentrations of each don’t matter as long as fluoride can adsorb to PaCl and
form flocs.
2. Allow a floc blanket to build up partially in the sedimentation tube.
3. Stop running the experiment. Run JustWater to push the floc blanket out of the sed tube
4. Watch the turbidimeter. It should spike from ~0.1 (or less) to 1 or 2. This rise in turbidity indicates flocs exiting the sedimentation tube.
5. With a bottle, collect samples of the effluent that had been through the turbidimeter. The sample should be rich in flocs.
4. Using the probe (that has been calibrated), measure the fluoride concentration of both samples.
5. Mix one of the samples by vigorously shaking for at least 10 seconds. This breaks up the flocs. Note which sample was mixed.
6. Using mesh, filter the samples to remove flocs and remeasure fluoride concentration.


## ProCoDA Method File

ProCoDA is a process control system that was developed by Monroe Weber-Shirk in order to set process parameters through a computerized system. It can be adjusted to different system states that control the system pumps depending on what flow rates are desired. Additionally, ProCoDA collects the data from probes, allowing for compilation of dye concentration data.

To begin the ProCoDA method file, three states were made: ON and OFF and Just Water. In the OFF state, all the valves were closed and no pumps were on. In the ON state, all the pumps were ON and all valves were opened, in the Just Water state, only the water valve was open. ProCoDA turned this pump on and off via a normal valve control, so long as the pump was already set to a proper flow rate. The system was set to run on Manual setting, as a proper run time had not yet been determined.

The method file was set to control the revolutions per minute (RPM) of the PACl/dye pump and the tap water pumps. This was done using the peristaltic pump ProCoDA file available in the AguaClara server as well as inputs for desired flow rate and tubing size. For the PACl and fluoride pump heads, inputs of $\mathrm{\frac{mL}{rev}}$ and flow rate were needed to calculate RPM since microtubing was used, and for the water pump head, tubing ID and flow rate were needed to calculate RPM. The set points used for the method file included a water pump set point for the water pump RPM and a floc pump set point for the PACl/dye pump RPM.

## Python Code

### Variables

```python
import math as m
from aguaclara.core.units import unit_registry as u
from aguaclara.core import physchem as pc
from aguaclara.core import utility as ut
import numpy as np

#Diameter of reactor tube
D_reactor = 1 * u.inch
#upflow velocity
V_up = 1.5 * u.mm/u.s
#Flow rate into reactor
Q_reactor = (m.pi*((D_reactor/2)**2)*V_up).to(u.mL/u.s)
#Height of reactor
H_reactor = 50 * u.inch
# Volume of reactor
Vol_reactor = (m.pi * ((D_reactor)**2)*H_reactor/4).to(u.mL)
# Residence time in reactor
T_residence= (Vol_reactor/Q_reactor).to(u.minute)



C_stock_PACl = 1000*u.mg/u.L
C_stock_dye = 1000*u.mg/u.L
C_reactor_PAC = 30*u.mg/u.L
C_reactor_F = 5*u.mg/u.L  

Q_stock_PAC = Q_reactor*(C_reactor_PAC/C_stock_PACl)

C_reactor_dye = (Q_stock_PAC*C_stock_dye)/Q_reactor

Q_tap = Q_reactor - 1*Q_stock_PAC
Q_fluoride = (0.5)*Q_tap

C_stock_F = Q_reactor*(C_reactor_F/Q_fluoride)

C_lab_PAC = 70900


#Flocculator Calculations

#Inputs
# flow rate in flocculator
Q_flocculator = Q_reactor
# target G*theta to design the flocculator
Gtheta_goal = 20000
#inner diameter of the flocculator tubing
D_floctube = 0.125 * u.inch
#radius of curvature (the radius of the tube the flocculator is wrapped around)
R_c = 4.25 * u.cm
```



```python
# To convert the document from markdown to pdf
pandoc Name_of_this_file.md -o TeamName_Research_Report.pdf
```
