# Bootstrapping Interview Guide

We will help you ace the Bootstrapping interview through our guide.

### **Level of Audience** <br>
This guide is aimed for anyone with some understanding of basic statistical concepts (confidence interval, p-value, linear regression, etc.) and is preparing for data scientist interviews.

This guide also assumes a basic familiarity of bootstrapping, for a detailed explanation of the basics of bootstrapping, see [here](bootstrap_basics.md).

### **Interview Questions you must know** <br>

**Q1:Could you briefly introduce bootstrapping concept in 1 minute?**

Ans: Bootstrapping is a resampling method with replacement which helps us to estimate the population, it could help us estimate the mean and standard deviation. Firstly, you can imagine if we have only one sample. We could apply resampling with replacement on this sample to build up the bootstrap sampling distribution. Then we could get the descriptive statistics from this distribution.

**Q2:What are the difference between sampling distribution and bootstrapping distribution?**

Bootstrapped distribution came from original sample, while sampling distribution came from population.

Bootstrapped distribution approximate sampling distribution as n gets larger, it dependeds on bootstrap sample we get.

**Q3:What are pros and cons of bootstrapping?**
Pros
1.Resolve resource limitation
2. Work with any population distribution

Cons
1.Excessive computing power
2.Rely on sample quality

**Q4:Tell me about how bootstrapping can be applied in linear regression models?**

Bootstrapping is a nonparametric approach to statistical inference that gives us standard errors and confidence intervals for our parameters
Bootstrap can be applied to regression models to give insights into variability of our parameters (beta) with minimal assumption about parent distribution
Parametric bootstrapping — resampling from all of the points (X):
1.Sample the data with replacement numerous times (100)
2.Fit a linear regression to each sample
3.Store the coefficients (intercept and slopes)
4.Plot a histogram of the parameters
5.Make inferences about true parameters

**Q5:Tell me why and how to apply bootstrapping on AB Testing??**

You can imagine you are data scientist in a gaming company, and you were assigned a AB Testing task.
Here is the Hypothesis: Where we should put the first gate? Level 30 vs. Level 40

