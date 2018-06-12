```python
import math as m
import numpy as np
from aide_design.play import*
import aide_design.floc_model as fm

#Q=.76*(u.milliliter)/(u.second)
#Q.to(u.m*u.m*u.m/u.s)
D=(1)*u.inch
D=D.to(u.m)
A=np.pi*(D**2)/4
print(A)
v=(0.002)*(u.m/u.s)
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
