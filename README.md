# Experiment
#Table 1

import matplotlib.pyplot as plt
import pandas as pd
data={'mg':[500,200,300,600,150,400],'t10':[6.07,4.54,4.88,7.06,3.72,5.25]} 
df=pd.DataFrame(data)
print(df)

df

df['t_10']= df.apply(lambda row: row.t10/10, axis= 1) 
print(df)

df

df['t2'] = df.apply(lambda row: row.t_10**2, axis =1)
print(df)

df

#table 2
import matplotlib.pyplot as plt
import pandas as pd
data2={"body      ":["light Body (m1)","Heavy Body(m**2)"],"T10":[3.87,4.69]}
df2= pd.DataFrame(data2)
print(df2)

df2

df2['T10_10']= df2.apply(lambda row: row.T10/10 , axis=1)
print(df2)

df2

df2['T2']= df2.apply(lambda row: row.T10_10**2 , axis=1)
print(df2)

df2

mass=[230,300]
df2["mi"]=mass

df2

#table 3

import matplotlib.pyplot as plt
import pandas as pd
data3 = {'W (dyne)' : [100000 , 250000], 'mg (g)': [102.040 , 225.102]}
df3 = pd.DataFrame(data3)
print (df3)

df3

import matplotlib.pyplot as plt
import numpy as np

xpoints = np.array([150,200,300,400,500,600])
ypoints = np.array([0.14,0.2,0.23,0.27,0.36,0.49])
plt.xlabel("Mass(g)")
plt.ylabel("Time(s^2)")
plt.title("Mass vs time^2", fontsize=20)
plt.plot(xpoints, ypoints,'o', ms=10, mec='hotpink', mfc='hotpink')
plt.show()

xpoints = np.array([100, 600])
ypoints = np.array([0, 0.50])
plt.xlabel("Mass(g)")
plt.ylabel("Time(s^2)")
plt.title("Mass vs time^2", fontsize=20)
plt.plot(xpoints, ypoints, color='hotpink')
plt.show()

#find the ratio mi1/mi2
mi1=150
mi2=400
ratio= mi1/mi2
r=round(ratio,3)
print(r,"g")

#find the ratio mg1/mg2
mi1=102.040
mi2=225.102
ratio2= mi1/mi2
r2=round(ratio2,3)
print(r2,"g")
