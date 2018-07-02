[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> 
First I found the mean of the first babies and the mean of the other babies
```python
import first
import thinkstats2

live, firsts, others = first.makeframes()
mean_firsts = firsts.totalwgt_lb.mean()
mean_others = others.totalwgt_lb.mean()
```
Which were 7.201094430437772lbs and 7.325855614973262lbs, respectively.

Next, I determined the difference between the two means

```python
mean_difference = mean_firsts - mean_others
```
Which was -0.12476118453549034 lbs. Thus, babies born first are on average 0.125 pounds lighter.

Next, I caclulated the difference relative to the mean of all (live) births
```python
mean_all = live.totalwgt_lb.mean()
percent_diff = (mean_difference/mean_all)*100
```
Which was -1.7171423678372415. Thus, babies born first are on average 1.72% lighter!

Lastly, I calcuated the Cohen effect size to quantify the difference between the two groups
```python
d = thinkstats2.CohenEffectSize(mean_firsts, mean_others)
```
Which was -0.088672927072602. Being first  has a larger absolute effect (and a negative effect) on baby weight than it does on pregnancy length, which has a positive cohen effect of (0.028879044654449883).
