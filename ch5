import numpy as np
import seaborn as sns
from scipy.stats import poisson, binom
import matplotlib.pyplot as plt

'''two ways to simulate poisson distribution'''
# scipy.stats simulation
for i in range(1000, 1001):
    data_binom = binom.rvs(n=i,p=0.8,size=10000)
    ax = sns.distplot(data_binom,
                      kde=True,
                      color='yellow',
                      hist_kws={"linewidth": 15,'alpha':1})
    ax.set(xlabel='Binomial Distribution', ylabel='Frequency')

    data_poisson = poisson.rvs(mu=int(i*0.8), size=10000)
    ax = sns.distplot(data_poisson,
                      bins=300,
                      kde=True,
                      color='skyblue',
                      hist_kws={"linewidth": 15,'alpha':0.4})
    ax.set(xlabel='Poisson Distribution', ylabel='Frequency')

plt.show()

# # numpy simulation
s = np.random.poisson(50, 1000)
count, bins, ignored = plt.hist(s, 15, normed=True, color='blue', alpha=0.4)

n, p = 10, .5
s_b = np.random.binomial(n, p, 100000)
count_b, bins_b, ignored_b = plt.hist(s_b, 30, normed=True, color='yellow')
plt.show()

'''some properties'''
# # ch5 (iii)-(a)
s0 = np.random.poisson(50, 1000)
count0, bins0, ignored0 = plt.hist(s0, 15, normed=True, color='blue', alpha=0.4)

s1 = np.random.poisson(20, 1000)
count1, bins1, ignored1 = plt.hist(s1, 15, normed=True, color='yellow')

s2 = np.random.poisson(30, 1000)
count2, bins2, ignored2 = plt.hist(s2, 15, normed=True, color='green', alpha=0.3)

s3 = s1 + s2
count3, bins3, ignored3 = plt.hist(s3, 15, normed=True, color='red', alpha=0.4)
plt.legend(['lambda=50', 'lambda=20','lambda=30', '20+30'])
plt.show()



