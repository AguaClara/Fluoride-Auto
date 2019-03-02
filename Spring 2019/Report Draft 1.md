# Fluoride Automated System, Spring 2019
#### Dominic Grasso, Melissa Louie, Desiree Sausele, Emily Spiek
#### February 22, 2019

**[Sidney: Hey team! I will be using bolded square brackets to comment on your manual.]**

## Abstract
The Fluoride Auto subteam seeks to develop a sustainable, inexpensive fluoride removal system for AguaClara plants in India.  Due to gel formation events in the sedimentation tube last semester, the team conducted test runs with red dye to monitor for gel formation.  Since no gel formation was observed, this event was likely a result of a shorter flocculator used by the Fall 2018 team. The Spring 2019 team will continue to develop a model to predict an optimal coagulant dosage given both influent and target effluent fluoride concentrations and research removal techniques for fluoride and arsenic from wastewater.

**[In future submissions, speak less about what previous teams did and more about your work. The Abstract is meant to give a brief overview of your semester's research.]**

**[Overall comment: Please remember to write in past tense throughout the manual as it would be someone in the future~ reading your final manual. Refer to Will's Technical Writing Presentation or our team's Grammar Guidelines on [Confluence](https://confluence.cornell.edu/display/AGUACLARA/Grammar+Guidelines+for+Reports).]**

## Introduction
Fluoride, in moderation, can provide a variety of healthy benefits. It can prevent tooth decay and, over time, strengthen teeth. An overexposure to fluoride, however, can cause dental fluorosis among other health issues. **[Good introduction to the problem you are addressing!]** In India, 85.0% of drinking water is sourced from groundwater, but this groundwater often displays excess levels of fluoride due to rocks in aquifers that leak large amounts of fluoride into the water. The prevalence of dental fluorosis, an indicator of excessive fluoride concentrations, differs across India, but has been shown to range from 13-91 percent depending on the age group in question and the water source supplying the state or municipality [(Arlappa et al., 2013)](http://www.ijrdh.com/files/11.Fluorosis.pdf).

In accordance with AguaClara's mission to create affordable, reliable, and sustainable water treatment solutions, the goal of the subteam is to treat groundwater that contains excessive fluoride concentrations. Teams from previous semesters analyzed the efficiency of fluoride removal by passing a coagulant, polyaluminum chloride (PACl), and a solution of fluoride through a sand filter. However, the sand filter was an inefficient method of removal because of the buildup of headloss from particles deposited in the sand filter that eventually prevented water from flowing through [(Dao et el., 2015)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride). Thus, instead of using a traditional sand filter, the team researched a similar relationship between PACl and fluoride via a floc blanket reactor. Flocs are aggregates of particles that are created through collision and precipitate out into the water. In the floc blanket reactor, flocs of PACl and clay adsorbed the fluoride from the influent water. The flocs then overflowed into a floc weir as the floc blanket grew and the purified water flowed out the top of the reactor. This reactor was modeled after the floc blanket, floc weir, and plate settlers setup in the sedimentation tank of a typical AguaClara water treatment plant. **[Briefly introduce the concepts of a floc blanket, floc weir, and plate settlers. Perhaps including a figure of these components would be helpful in introducing them/making them clear to the reader what they are?]** The team expected that the floc blanket reactor would be able to remove fluoride with a significantly higher efficiency than the sand filter from previous semesters and could run for extended periods of time due to the absence of headloss buildup in the reactor. The flocs in the floc blanket could exit the floc weir while the fluoride in the sand filter would build up and saturate the sand in a short amount of time [(Longo et al., 2016)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride) [(Cheng et al., 2016)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride).

The main goal of Fluoride Auto subteam thus far has been to analyze fluoride removal by researching and constructing Langmuir isotherms. Langmuir isotherms are used to explain adsorption mechanisms. They are based upon the assumptions that there are a fixed number of adsorption sites and each site can hold one adsorbed molecule. The Fall 2018 team fit a Langmuir isotherm to previous data obtained in Fall 2017 and Summer 2018 by Fluoride subteams. After discovering issues with various data points, the Langmuir isotherm plots were constructed with the removal of some data points. Once the Langmuir isotherm is verified, the information can be applied to other dissolved species removal teams in AguaClara.

The Fall 2018 Fluoride Auto subteam faced the issue of gel formation in their floc blanket reactor, which prevented the floc blanket from exiting through the weir. The cause of the gel formation was not entirely known but was theorized to have occurred due to an oversaturation of flocs in the floc blanket. The Spring 2019 team, therefore, aimed to reconstruct the reactor with the weir in a lower position. In the future, the team will attempt to validate the Langmuir isotherms constructed by teams in previous semesters. The team will also attempt to determine a safe method of disposal for fluoride after it has been removed from the drinking water. This course of action, when determined, will be essential in the implementation of fluoride-removal plants in India.

**[Great intro!! I love how you guys explained your problem from the beginning so that it is clear to the reader what issue you are addressing and why it's important.]**

## Literature Review
#### *Fluoride Limitations and Hazards*
Though in small quantities fluoride can be beneficial to human health, over-consumption of fluoride can lead to a number of health concerns, including arthritis, dental fluorosis, bone deformation, and ligament calcification [(Roholm, 1937)](http://cof-cof.ca/wp-content/uploads/2012/10/Roholm-Fluorine-Intoxication-A-Clinical-Hygienic-Study-Copenhagen-Denmark-1937.pdf). Touching, digesting, and even inhaling fluoride can lead to damaged eyes and skin [(NJ Department of Health, 2010)](http://nj.gov/health/eoh/rtkweb/documents/fs/1699.pdf). According to the National Research Council (NRC), the maximum contaminant level (MCL) of fluoride in drinking water is 4 $\mathrm{\frac{mg}{L}}$. However, a secondary limit of 2 $\mathrm{\frac{mg}{L}}$ has been established by the EPA to avoid potential cosmetic effects such as tooth and skin discoloration. The World Health Organization (WHO) established a safe upper limit of 1.5 $\mathrm{\frac{mg}{L}}$ to avoid all potential risks of fluoride consumption. Groundwater fluoride levels in India vary from 5 to 23 $\mathrm{\frac{mg}{L}}$, which is well above any established recommended limit and has caused many of the aforementioned health concerns in communities with contaminated water. [(LeChevallier and Au, 2004)](http://www.who.int/water_sanitation_health/publications/9241562552/en/). The Fluoride Auto subteam strives towards the WHO guideline of 1.5 $\mathrm{\frac{mg}{L}}$ of fluoride when designing and experimenting with the floc blanket reactor and manipulating the ratios and concentrations of PACl in the system.
#### *Polyaluminum Chloride (PACl) and Fluoride Removal*
AguaClara water treatment consists of a series of coagulation, flocculation, and clarification. During coagulation, raw water is mixed with a positively charged coagulant (typically an aluminum salt or iron salt), altering or destabilizing any negatively charged particles or dissolved and colloidal contaminants [(EPA, 2016)](https://iaspub.epa.gov/tdb/pages/general/home.do). The destabilized particles then proceed through flocculation, where additional mixing increases the rate of particle collision, forming larger precipitates. Following the formation of flocs, clarification removes the agglomerated particles through sedimentation or other removal processes [(EPA, 2016)](https://iaspub.epa.gov/tdb/pages/general/home.do).

Recently, polymerized forms of aluminum salts have begun to replace standard aluminum salt coagulants [(Ingallinella and Pacini, 2001)](https://www.tandfonline.com/doi/full/10.1080/10934529.2011.598835?scroll=top&needAccess=true). Polyaluminum chloride (PACl), a partially hydrolyzed aluminum salt, is one of the most widely used, as it delivers results similar to those of aluminum sulfate (alum) coupled with a polyelectrolyte [(Ingallinella and Pacini, 2001)](https://www.tandfonline.com/doi/full/10.1080/10934529.2011.598835?scroll=top&needAccess=true). Using PACl instead of alum leads to a reduction in sulfates added to treated water, lower sludge production, reduced odor problems, and higher overall removal efficiency [(Gebbie, 2001)](http://wioa.org.au/conference_papers/2001/pdf/paper6.pdf). PACl is also less sensitive to temperature changes in its hydrolyzed state and has a broader range of raw water pH in which it is an effective coagulant [(EPA, 2016)](https://iaspub.epa.gov/tdb/pages/general/home.do) [(Yang et al., 2010)](https://www.ncbi.nlm.nih.gov/pubmed/20188465).  For the removal of fluoride, specifically, PACl has been found to be the most effective with pH values between 5.2 and 6.2 [(EPA, 2016)](https://iaspub.epa.gov/tdb/pages/general/home.do). For fluoride removal, PACl appears to be the optimal coagulant [(Zonoozi et al, 2009)](https://www.ncbi.nlm.nih.gov/pubmed/19381000). **[Awkward wording for the last sentence? This paragraph just reads like you are spitting out facts. To wrap it up, maybe you could say "Therefore, PACl appears to be the optimal coagulant for fluoride removal."]**

Current fluoride removal processes need improvement. The Nalgonda technique is a common fluoride removal method that involves a combination of rapid mixing, flocculation, sedimentation, filtration and disinfection [(Kumbhar and Salkar, 2014)](http://www.ijetae.com/files/Volume4Issue10/IJETAE_1014_22.pdf). Unlike AguaClara treatment, which is a continuous flow process, the Nalgonda technique is a "batch filtration" method, where large quantities of water are treated in buckets. A series of treatments to obtain safe, treated water for extended periods of time, so currently the Nalgonda technique is largely used as a household treatment method. It has been introduced to various Indian villages, including those in Nalgonda and in the state of Telangana. It is also currently being studied at the pilot scale in Kenya, Senegal and Tanzania [(Dahi et al., 1996)](https://wedc-knowledge.lboro.ac.uk/resources/conference/22/Dahi.pdf).  In addition to the restrictions implied by batch treatment, the Nalgonda method requires a high dosage of aluminum sulfate to aggregate with fluoride and precipitate. A study conducted by [(Dahi et al., 1996)](https://wedc-knowledge.lboro.ac.uk/resources/conference/22/Dahi.pdf) suggests that 13 $\mathrm{\frac{g}{L}}$ alum (1.2 $\mathrm{\frac{g}{L}}$ as Al) is needed for the Nalgonda method to effectively treat fluoride levels between 9 and 13 $\mathrm{\frac{mg}{L}}$. Despite the high concentrations of coagulant, the fluoride residual in the test was still unable to meet the WHO safety guidelines of 1.5 $\mathrm{\frac{mg}{L}}$ of fluoride. The high dose of aluminum sulfate also leaves high sulfate residuals in the water, which causes taste and odor issues [(Bailey and Fawell, 2004)](http://apps.who.int/iris/handle/10665/43514). In regards to other filtration methods, a study by Inganiella achieved 33.3% removal of fluoride using a combination of a gravel pre-filter and a sand rapid filter to capture granules of fluoride, PACl, NaClO and $SO_4H_2$ [(Ingallinella and Pacini, 2001)](https://www.tandfonline.com/doi/full/10.1080/10934529.2011.598835?scroll=top&needAccess=true). Though this clearly is not effective enough to obtain safe drinking water.
#### *Floc Blankets*
Floc blankets develop when vertical flow sedimentation tanks form a fluidized bed of particles. An example is shown in the figure below. A floc blanket then facilitates particle removal by “increasing particle-particle interactions that lead to flocculation and filtration occurring in the floc blanket” [(Hurst, 2010)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.849.6127&rep=rep1&type=pdf).

<div style = "text-align:center">
<img
align = "center"
src="https://github.com/AguaClara/fluoride/blob/master/fluoride%20report/Flocs_in_Reactor.jpg?raw=true" height=400, width=300>

Figure 1: Floc blanket forming in the reactor

</div>

The process of forming flocs requires both the precipitation of aluminum hydroxide from the coagulant and the contact with raw water colloidal particles [(Hurst, 2010)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.849.6127&rep=rep1&type=pdf). Once the combination of precipitation and mixing forms small particles, these new flocs collide to form larger, more porous flocs that can then be used for clarification [(Hurst, 2010)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.849.6127&rep=rep1&type=pdf). **[Define clarification.]**

This floc blanket clarification is considered hindered settling, which is a form of sedimentation [(Gregory et al., 1996)](https://link.springer.com/chapter/10.1007%2F978-3-642-61196-4_2). Sedimentation processes are characterized by the removal of suspended particles, e.g. flocs, sand, and clay, from water. Removal is possible due to the differences in density between water and the suspended particles, but is also dependent on the size of the suspended particles, water temperature, turbulence, stability of flow, bottom scour, and flocculation [(Sun, 2004)](http://onlinelibrary.wiley.com/doi/10.1002/0471623571.ch11/summary). Floc blanket clarification, however, is primarily driven by upflow velocity of the water and by floc concentration, while the other parameters show a weaker correlation with the creation of the floc blanket. [(Gregory et al., 1996)](https://link.springer.com/chapter/10.1007%2F978-3-642-61196-4_2). The relationship between upflow velocity, concentration and water quality can be combined into the mass rate of settling, which is equal to the product of upflow velocity and concentration. Within a range of mass fluxes, a distinct interface is established between clear water and the floc blanket and thus one can deduce appropriate values of velocity and floc concentration.  At concentrations above that ideal mass flux range, the aggregation of flocs becomes thick enough that compression settling occurs, which refers to when over a quarter of the volume of the coagulant will enter the floc blanket within an hour. At concentrations below that appropriate range, flocs are not inhibited by other particles and a suspension with different settling velocities is formed [(Gregory et al., 1996)](https://link.springer.com/chapter/10.1007%2F978-3-642-61196-4_2).
Examples of floc blanket clarification are shown throughout the world as further proof of its potential in water purification. In Taiwan, a process of pre-sedimentation, floc blanket clarification, and sand filtration is used to reduce 100 NTU water down to potable levels [(Lin et al., 2004)](https://ascelibrary-org.proxy.library.cornell.edu/doi/abs/10.1061/(ASCE)0733-9372(2004)130:12(1481)). Floc blankets have also been used extensively to purify water of algae, protozoa and specific virus strains [(LeChavallier and Au, 2004)](http://www.who.int/water_sanitation_health/publications/9241562552/en/). Therefore, it is believed that the adaptability of this method in conjunction with the use of PACl would allow for effective fluoride removal.

**[Very thorough and well-written Lit Review. I learned so much from you guys!]**

## Previous Works
Prior to the Spring 2016 semester, the team used a sand filter system that was inexpensive and thorough in removing fluoride per milligram of PACl used. However, the main issue with the sand filter was that it became saturated with PACl and fluoride within several hours, thus building up head loss and rendering the sand filter inefficient and inadequate at removing fluoride. Consequently, the system required backwashing every few hours, which was determined to be infeasible. In order to address these inefficiencies of the sand filter system, the team fabricated a new single floc blanket reactor [(Longo, 2016)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride) that mirrored that of the floc blanket and plate settlers present in the then-current Aguaclara plants. The team also implemented a new setup that included stock tanks, a reactor, a turbidimeter, a flocculator, and stock and waste pumps, which was consistent with previous research regarding quantity of coagulant added and head loss accumulation [(Dao, 2015)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride).

The Spring 2016 team then developed a MathCad file to calculate flow rates of pumps from a given set of parameters including upflow velocity, tubing diameters, and reactor concentrations. The team also created a ProCoDA method file to turn the flow rates into RPMs for the pumps so that the process of changing PACl and fluoride concentrations within the reactor was more user-friendly. Transitioning the MathCad file completely to Python is still underway, but might not be necessary if the gravity-powered setup is successful.

In the Fall 2016 semester, the team fabricated a new bottom insert to prevent the accumulation of flocs that previously clogged the bottom of the reactor. The newly designed geometry incorporated a smooth sloped bottom, as shown in Figure 3, **[Are you missing a figure?]** which allowed for gradual flow expansion and recirculation of flocs that would have settled to the bottom of the reactor with the old bottom geometry. The formation of gels during experiments in Fall 2018 has many potential causes, one of which was thought to be the bottom geometry. **[Don't suddenly start talking about the research of another semester while you're in the middle of discussing a different one! This is very confusing.]** Further research into that is currently underway.

The team also determined the minimum length of the reactor needed to save resources and space. A shorter reactor, with a height of 5 cm below the weir, was tested with concentrations of 25 $\mathrm{\frac{mg}{L}}$, 50 $\mathrm{\frac{mg}{L}}$, and 100 $\mathrm{\frac{mg}{L}}$ of dye. Although the floc blankets reached a short term steady state height of around 20-30 cm, in the long term the flocs built up and traveled through the tube settler to the turbidimeter, indicating a failure in the reactor. This observation suggested that there was some minimum height that a floc blanket would reach, and the team concluded that a shorter reactor system was not feasible [(Longo, 2016)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride).

In the summer of 2017, the fluoride team repeated tests from the previous semester to determine whether the improvements made by the second reactor in series were significant enough to warrant implementation on a larger scale. The summer 2017 team stopped adding clay to the system and focused on the goal of determining a PACl concentration that would optimize fluoride removal rates [(Longo, 2017)](https://confluence.cornell.edu/display/AGUACLARA/Fluoride), which is the main objective of the team. Initial tests indicated reactor failure within 10 hours due to sludge buildup regardless of PACl concentration, so the team switched to using a new reactor designed by the summer 2017 High Rate Sedimentation team. This new reactor increased the time to failure and allowed for higher upflow velocities. After running various tests, the team determined that an upflow velocity of 1.5 $\mathrm{\frac{mm}{s}}$ was the best way to reduce sludge buildup. The team then ran experiments to examine the effect of higher PACl concentrations on removal rates. Data collected from these experiments was used to create an adsorption model that could calculate the necessary PACl dosage for a desired effluent fluoride concentration.

After creating the adsorption model, the team observed a significant difference in the fluoride probe readings for tap water versus the readings in deionized water. The findings suggested that the amount of fluoride ions in tap water is actually higher than the readings from the fluoride probe state. Therefore, the team deemed the adsorption model to be inaccurate and planned to revise it, taking this discrepancy into consideration.

In the Spring 2018 semester, experiments were conducted with a new fluoride probe, which measured the effluent concentrations of fluoride after treatment with different concentrations of PACl. When a new probe was used, the difference in voltage readings between tap and DI water turned out to be negligible; therefore, it was concluded that the discrepancy last semester may have been caused by a probe issue. The results are summarized in the table below. **[Refer to the table as Figure 2 so it's more clear what you're talking about.]**

<div style = "text-align:center">
<img
align = "center"
src="https://github.com/AguaClara/fluoride/blob/master/fluoride%20report/Results.png?raw=true" height=200 width=220>

Figure 2. A summary of the experimental results of final fluoride concentrations based on varied concentrations of initial and PACl concentrations.

<div style = "text-align:left">

In the summer of 2018, the team ran experiments to measure the effluent concentrations of fluoride for different concentrations of PACl to construct an adsorption model, which could be used to predict the PACl dosage required for a desired effluent fluoride concentration and would generate an adsorption density value for the mass of fluoride adsorbed (W). The WHO standard for fluoride levels is 1.5 $\mathrm{\frac{mg}{L}}$, which is the desired effluent fluoride concentration. Therefore, the model would calculate a range of uptake values that would result in the target effluent concentration. In addition, the model would provide a way to calculate the PACl dosage required to treat an initial fluoride concentration given a range of W values.

The findings of the Summer 2018 team showed that the reactor would clog due to insufficient shear to break down the PACl flocs, which then caused the bed to fluidize. This result indicates that, for an excessive PACl dosage, a second reactor would be necessary to decrease the maximum concentration of PACl needed to run the system. The Fall 2018 **[I think you're missing the word "team" here. Also, I said this already but don't suddenly start talking about another team when you're already discussing one.]** later confirmed this result with the observation of gel systems forming at high PACl concentrations.

However, the Summer 2018 team found that results were inconclusive. For example, influent concentrations of 10 $\mathrm{\frac{mg}{L}}$ and 5 $\mathrm{\frac{mg}{L}}$ of fluoride resulted in the same fluoride effluent concentration of around 3 $\mathrm{\frac{mg}{L}}$ for 12.5 $\mathrm{\frac{mg}{L}}$ of PACl and around 2 $\mathrm{\frac{mg}{L}}$ for 25 $\mathrm{\frac{mg}{L}}$ PACl. It is unlikely that the same dosage of PACl would result in the same effluent fluoride concentration for fluoride inlet concentrations that differ as substantially as by a factor of 2. Therefore, another more accurate probe should be ordered before any definitive conclusions can be drawn.

The team then began using the probe that had been ordered in May 2018 for experiments that used the isotherm developed by the Spring 2018 team to change the coagulant dosing. The experiments showed that a 6.25 mg/L dosing of coagulant did not create a floc blanket. As a result, the coagulant dosing used in subsequent experiments ranged from 10 mg/L to 50 mg/L with the influent fluoride concentration ranging from 3 mg/L to 20 mg/L. The team also identified that the influent fluoride concentration did not match the ideal concentration set by the flow rate and stock tank concentration. Therefore, the team began to take manual readings of the influent fluoride before it reached the flocculator to compare with the effluent fluoride reading. These manual readings were used for the Langmuir isotherm derivation in the fall **[Capitalize Fall.]** of 2018.

The Fall 2018 team created a longer reactor due to a low upflow velocity, in accordance with the findings of the Fall 2016 team discussed previously regarding reactor length. The main goal of this past semester was to analyze the Fall 2017 and Summer 2018 Langmuir isotherm that modeled the adsorption of fluoride to PACl. The team used the experimental data from the two previous teams to graph a nonlinear regression to compare the experimental results to the theoretical Langmuir isotherm. The analysis showed that the data closely fit the adsorption model, especially at low concentrations of fluoride. The team also calculated a coefficient of determination of 0.82, indicating that a high percentage of variability in the uptake occurs because of the variability in concentration. While more data is still necessary to confirm the Langmuir isotherm, the team concluded that the model so far is sufficient to predict required PACl concentrations based on fluoride concentrations.

<div style = "text-align:center">
<img
align = "center"
src="https://github.com/AguaClara/Fluoride-Auto/raw/master/langmuir.PNG?raw=true" height=200 width=220>

Figure 3. The experimental data from Fall 2017 and Summer 2018 plotted against the theoretical Langmuir isotherm.

<div style = "text-align:left">

**[Refer to your figure in your writing so when skimming your paper, it is obvious to the reader which figures go with what information in your report.]**

The Fall 2018 team then implemented a new bottom geometry into the reactor system to reduce variability. This new bottom geometry was designed with the intent of guiding flocs to flow parallel to each other and prevent them from colliding and accumulating. However, when the new design was implemented, the formation of a super saturated solution and **[insert commas here before and after "subsequently" otherwise the first part of your sentence reads as a fragment]** subsequently gel occurred. The first experiment in which gel appeared in the reactor was with a concentration of 40 mg/L PACl and 10 mg/L fluoride. The team hypothesized that either the concentration of PACl was too high or the ratio of fluoride to PACl was too high. Previous experiments were run with up to 50 mg/L PACl concentration without gel formation. Additionally, an aluminum fluoride complex may have formed and repelled other aluminum particles within the solution. While past teams have conducted experiments at higher fluoride concentrations, few experiments were conducted at concentrations of 10 mg/L or higher. The second theory is consistent with this semester's experiments in that the inclusion of the bottom geometry increases gel formation.

In order to more clearly observe the gel formation, the team injected red dye into the sedimentation tube with the PACl. Using this method, the team concluded that gel first formed in the floc hopper and accumulated until it reached the top of the reactor because of the flow of dye throughout the reactor. The gel only dissociated within the reactor with an upflow velocity of 8 mm/s. The gel within the floc weir was more difficult to remove because it was controlled by a single speed pump.

Further experimentation was conducted by replacing the fluoride stock with red dye to produce more visible flocs. The first experiment, which was run with 20 mg/L PACl, showed formation of flocs and later aggregation of the flocs into a gel at the entrance to the floc weir. The team hypothesized that the protrusion of the floc weir into the sedimentation tube provided a surface for flocs to accumulate and form gel. A new sedimentation tube was fabricated to test the hypothesis, and the red dye experiment was replicated in the new tube. The experiment resulted in gel formation, however, flocs entered the floc weir without aggregation at the entrance as observed in the previous reactor. The team hypothesized that gel formed when the flocs that were above the floc weir descended down the sedimentation tube and collided with other flocs, which created a super saturated solution necessary for a gel.

The team continued to run tests at low concentration of PACl, or a maximum of 20 mg/L, and high concentrations of red dye given the dilute stock solution of red dye. However, each experiment gelled, and thus, produced no useful data for further validating a Langmuir adsorption model.

**[Great work overall! You are so thorough in each of the sections you worked on. Sometimes you get lost in your own work though forget to define terms, which is an easy fix! Please address my and Tigran's comments for the next report and you should be good to go!]**

## Methods
Explain the techniques you have used to acquire additional data and insights. Reserve fine detail for the Manual at the end of the report, but use this section to give an overview with enough detail for the reader to understand your Results and Analysis. Describe your apparatus, and have a justification for every decision you made and every parameter you chose in the design of the apparatus. Be especially careful to detail the conditions your experiments were conducted under, as this information is especially important for interpreting your results

Below, some example sections are given. Sectioning the report is meant to keep similar information together.  Continue making sections as necessary, or delete sections if you do not need them. Feel free to add subsubsections to further delineate the information. For example, under the Experimental Apparatus section below, the EStaRS team might consider having sections such as "Filter Design" and "Filter Fabrication".

### Experimental Apparatus
Explain your apparatus setup using enough detail such that future teams can recreate your apparatus. Make sure to explain why you built it this way.
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

Yang, Z. L., Gao, B. Y., Yue, Q. Y., and Wang, Y. (2010). Effect of pH on the coagulation performance
of Al-based coagulants and residual aluminum speciation during the treatment of humic acid–kaolin
synthetic water. Journal of Hazardous Materials, 178(1):596–603.

Zonoozi, M. H., Moghaddam, M. A., and Arami, M. (2009). Coagulation/flocculation of dye-containing
solutions using polyaluminium chloride and alum. water science and technology, 59(7):1343–1351.

# Manual
The goal of this section is to provide all of the guidance that would be necessary for a future team to pick up your work where you left off. Please try to be thorough and put yourselves in the shoes of a newcomer to the project. Below are some recommended sections, but the manual will likely take a slightly different form for each team.

## Fabrication Details
Include any information related to the fabrication of equipment, experimental apparatuses, or technologies. Include the purpose of each step and the fabrication methods used. Reference appropriate safety precautions.

## Special Components
If your subteam uses a particular part that is unique and you could foresee a future subteam needing to order it or learn more about it, please include basic information like the vendor where it was purchased, catalog/item number, and a link to any documentation.

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
# Comment
```

# Add/Delete/Change this Template as you see Fit
When using this template keep in mind that this serves three purposes. The first is to provide your team feedback on your progress, assumptions, and conclusions. The second is to keep your team focused on what you are learning and doing for AguaClara. Another is to educate future teams on what you've learned and done. This document should be comprehensive, consistent, and well-written. With that in mind, add, subtract, or move sections. Reach out to the RAs and graders for help with figuring out what should or shouldn't include. Focus on how wonderful a reference you are making through this and work hard on communicating amongst yourselves and with future teammates. (Delete this section before submitting)

```python
# To convert the document from markdown to pdf
pandoc Name_of_this_file.md -o TeamName_Research_Report.pdf
```
