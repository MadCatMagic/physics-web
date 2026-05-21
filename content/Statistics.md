---
tags:
  - stats
date-created: 2025-12-17
template-version: m.0
---
[[Data Analysis & Stats L_MT1]]
### Errors
#stats/st-error 
When we take multiple measurements, they will follow some random distribution $X$. This distribution will have an inherent standard deviation and mean, which will not change - no matter how many readings we take the st. dev will not decrease. However we want a true value so we take the standard error $\alpha$ which is the standard deviation of sample means.
$$
\sigma(X)^{2}=\frac{1}{N}\sum_{i=1}^{N} (x_{i}-\bar{x})^{2}
$$
$$
\alpha(X)=\frac{\sigma(X)}{\sqrt{ N }}
$$
This is due to the central limit theorem which states that the distribution of sample means always approaches a normal distribution whatever the underlying distribution.
#stats/central-limit-theorem 

### Error Propagation
#stats/error-propagation 
Errors are added in quadrature for proper calculus based propagation:
$$
\Delta f^{2}=\left( \frac{ \partial f }{ \partial x_{1} } \Delta x_{1} \right)^{2}+\left( \frac{ \partial f }{ \partial x_{2} } \Delta x_{2} \right)^{2}+\dots
$$

### Weighted Mean
#stats/weighted-mean 
If you have a set of data points with associated error values then we can calculate a weighted mean; each value $x_i$ has an associated $w_{i}$ so we have
$$
\bar{x}=\frac{{\sum x_{i}w_{i}}}{\sum w_{i}}
$$
then for the error $\sigma_{i}$ in each measurement we get $w_{i}=\frac{1}{\sigma_{i}^{2}}$ as the weights. Hence:
$$
\bar{x}\pm\alpha=\frac{\sum \frac{x_{i}}{\sigma_{i}^{2}}}{\sum \frac{1}{\sigma^{2}_{i}}}\pm \sqrt{ \frac{1}{\sum \frac{1}{\sigma_{i}^{2}}} }
$$
### Error analysis
#stats/least-squares 
When we are analysing data we use the least squares heuristic for finding relationships. This means that e.g. a linear fit minimises the least squares value:
$$
s=\sum_{i=1}^{N} (y_{i}-y_{\text{fit}})^{2}
$$
We also can plot the residuals $y_{i}-y_{fit}$ to look for a pattern in them that would suggest the fit was improper - they should appear randomly distributed around 0.

#stats/chi-squared 
Another method of analysis is to take the chi-squared value
$$
\chi^{2}= \sum_{i=1}^{N} \frac{({O_{i}-E_{i}})^{2}}{E_{i}}
$$
where $O_{i}$ is the original value and $E_{i}$ is the expected value. We can compare this with the distribution to identify how strong the correlation is for a given number of data points.