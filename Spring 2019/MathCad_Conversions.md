#MathCad Conversions
March 11, 2019

```python
import math as m
from aguaclara.core.units import unit_registry as u
from aguaclara.core import physchem as pc
from aguaclara.core import utility as ut
import numpy as np

#Diameter of reactor tube
D_reactor = 1 * u.inch
#upflow velocity
V_up + 1.5 u.mm/u.s
#Flow rate into reactor
Q_reactor = math.pi*((D_reactor/2)**2)*V_up
#Height of reactor
H_reactor = 50 u.in
Vol_reactor = math.pi
