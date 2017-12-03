[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

My code:
``` python
import numpy as np
import thinkstats2
import thinkplot

sample = np.random.random(1000)

sample_pmf = thinkstats2.Pmf(sample, label='sample')
thinkplot.Pmf(sample_pmf)
thinkplot.Config(xlabel='Number', ylabel='Pmf')

sample_cdf = thinkstats2.Cdf(sample, label='sample')
thinkplot.Cdf(sample_cdf)
thinkplot.Config(xlabel='Number', ylabel='CDF', loc='upper left')
```

For random numbers, it looks like they are properly randomly distributed.  The PMF is uniform with a max of 0.001 percent which means there are no duplicate numbers and all numbers had the same probability of appearing. Then when we max the Cdf, we get close to a straight line with a slope of 1, which would mean that everything has equal odds of appearing
