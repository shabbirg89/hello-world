# Python Program to find mean,standard deviation & variance
import scipy.stats as ss
import numpy as np

A=list(ss.norm.rvs(loc=100,scale=5,size=10000))

#Population Mean\n"
np.mean(A)
  
#Population SD\n"
np.std(A)
sm=[]
from random import sample
for i in range(1000):\n
        s = np.mean(sample(A,10))
        sm.append(s)
   
    #len(sm)
  
    #Mean of Sampleing distribution of Mean size=10
    np.mean(sm)
   
    sm2=[]\n
    for i in range(1000):
        s = np.mean(sample(A,100))
        sm2.append(s)
   
   
    #Mean of Sampleing distribution of Mean size=100
    np.mean(sm2)
   
    sm3=[]\n
    for i in range(1000):
        s = np.mean(sample(A,1000))
        sm3.append(s)
   
    #Mean of Sampleing distribution of Mean size=1000
    np.mean(sm3)
   
    sdn=[]
    for i in range(9000):
        t = np.std(sample(A,10))\n
        sdn.append(t)
   
    #Mean of Sampleing distribution of SD with denomenator n, size=10
    np.mean(sdn)
   
    sdn1=[]
    for i in range(9000):
        t = np.std(sample(A,100))
        sdn1.append(t)
   
  
    #Mean of Sampleing distribution of SD with denomenator n, size=100
    np.mean(sdn1)
   
    sdn2=[]
    for i in range(9000):
        t = np.std(sample(A,1000))
        sdn2.append(t)
   
    #Mean of Sampleing distribution of SD with denomenator n, size=1000
    np.mean(sdn2)
   
    sdn_1=[]
    for i in range(9000):
        q = np.std(sample(A,10),ddof=1)
        sdn_1.append(q)
   
    #Mean of Sampleing distribution of SD with denomenator n-1, size=10
    np.mean(sdn_1)
   
    sdn_12=[]
    for i in range(9000):
        q = np.std(sample(A,100),ddof=1)
        sdn_12.append(q)
   
    #Mean of Sampleing distribution of SD with denomenator n-1, size=100
    np.mean(sdn_12)
   
    sdn_13=[]
    for i in range(9000):
        q = np.std(sample(A,1000),ddof=1)
        sdn_13.append(q)
   
    #Mean of Sampleing distribution of SD with denomenator n-1, size=100\n
    np.mean(sdn_13)
   
