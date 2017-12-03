[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

My Code:
```python
import scipy.stats

mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)

height_low = dist.cdf(177.8)
height_high = dist.cdf(185.4)

height_high - height_low
```

For this answer we get 0.342. This was calculated by getting the percentile of people who are 6'01" (185.4 cm) and then subtracting the percetile of people who are 5'10" (177.8 cm). This gets us 34% of the population that are between 5'10" and 6'01"
