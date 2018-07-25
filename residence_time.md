```python
import math as m
import numpy as np
from aide_design.play import*

#flocculator length
number_of_turns = 49
flocculator_diameter = 84.30 * u.millimeter
circumference = 2 * math.pi * (flocculator_diameter/2)
length = (number_of_turns * circumference)
d_flexible_tubing = 3 * u.millimeter
cross_section = math.pi * (d_flexible_tubing/2)**2
vol_flocculator = (cross_section * length).to(u.milliliter)

#sedimentation tube
diameter = (1 * u.inch).to(u.millimeter)
length = (98.5 * u.centimeter).to(u.millimeter)
A = math.pi * (diameter/2)**2
vol = (length * A).to(u.milliliter)

d_waste = (0.25 * u.inch).to(u.millimeter)
l_waste = (39 * u.centimeter).to(u.millimeter)
A_waste = math.pi * (d_waste/2)**2
vol_waste = (l_waste * A_waste).to(u.milliliter)

vol_sed = (vol + vol_waste).to(u.milliliter)

#total volume
V = vol_flocculator + vol_sed
Q = 0.76 * (u.milliliter/u.s)
residence_time = V/Q






```
