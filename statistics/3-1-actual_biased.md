[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

My Code:
```python

import nsfg
import thinkstats2
import thinkplot

def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf

resp = nsfg.ReadFemResp()
pmf = thinkstats2.Pmf(resp.numkdhh, label='actual')

biased_pmf = BiasPmf(pmf, label='observed')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Config(xlabel='Children in household', ylabel='PMF')

print('Actual mean', pmf.Mean())
print('Observed mean', biased_pmf.Mean())
```

The Results are:

Actual mean = 1.02420515504

Observed mean = 2.40367910066

This shows that a biased reporting sample could cause large differences in the mean from the actual distribution. Where the actual mean of childred in a family is 1.02, due to families with larger children counts appearing more often in a sample would change the mean to a biased mean of 2.40.
