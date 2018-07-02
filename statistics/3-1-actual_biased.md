[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> First I constructed actual distribution for the number of children under 18 in the household using the NSFG respondent variable NUMKDHH and getting its probability mass function (a map from each value to its probability).
```python
import nsfg
import thankstats2
import thinkplot
resp = nsfg.ReadFemResp()
actual_pmf = thinkstats2.Pmf(resp.numkdhh, label='actual')
```
Next, I computed the biased distribution if we were to survey children and asked them how many children under 18 (including themselves) are in their household by multipying each class size by the number of students who observe that class size.
```python
def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf
biased_pmf = BiasPMF(actual_dist, 'biased')
```
 Next, I plotted the actual and biased PMFs
 ```python
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Show(xlabel='class size', ylabel='PMF')
 ```
 
