[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> First, I imported scipy.stats to be able to access analytic distributions
```python
import scipy.stats
```
Next, I created a normal distribution representing the US male population's heights using the given parameters.

```python
mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)
```
Lastly, I calculated the percentage of the US male population between the range of 5'10"(177.8cm) and 6'1"(185.4cm)
by calculating the number of people below or equal 5'10" and the number of people below or equal to 6'1" using their CDFs and subtracting them.
```python
five_ten_or_below= dist.cdf(177.8)
six_one_or_below = dist.cdf(185.4)
between_range = six_one_or_below - five_ten_or_below
```
The percentage of the US male population between 5'10" and 6'1" is 0.34209468294595308 or ~34.2%
