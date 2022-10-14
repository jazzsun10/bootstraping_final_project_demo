# Bootstrapping Interview Guide

We will help you ace the Bootstrapping interview through our guide.

### **Level of Audience** <br>
This guide is aimed for anyone with some understanding of basic statistical concepts (confidence interval, p-value, linear regression, etc.) and is preparing for data scientist interviews.

*This guide also assumes a basic familiarity of bootstrapping, for a detailed explanation of the basics of bootstrapping, see [here](https://github.com/jazzsun10/bootstraping_final_project_demo/blob/main/Bootstrap_Basics.md).*

### **Interview Questions you must know** <br>

*See [here](https://github.com/jazzsun10/bootstraping_final_project_demo/blob/main/MSDS%20601%20Final%20Presentation-Bootstrapping.pdf) for a full pdf version of the guide with graphics.* 

**Q1: Could you briefly introduce bootstrapping concept in 1 minute?**

Ans: Bootstrapping is a resampling method with replacement which helps us to estimate the population, it could help us estimate the mean and standard deviation. Firstly, you can imagine if we have only one sample. We could apply resampling with replacement on this sample to build up the bootstrap sampling distribution. Then we could get the descriptive statistics from this distribution.


**Q2: What are the difference between sampling distribution and bootstrapping distribution?**

Bootstrapped distribution came from original sample (treating the sample as population), while sampling distribution came from population.

Bootstrapped distribution approximate sampling distribution as n gets larger, and the bootstrap distribution dependeds on sample we get.


**Q3: What are pros and cons of bootstrapping?**

Pros

1.Resolve resource limitation

2.Work with any population distribution

Cons

1.Excessive computing power

2.Rely on sample quality


**Q4: Tell me about how bootstrapping can be applied in linear regression models?**

Bootstrapping is a nonparametric approach to statistical inference that gives us standard errors and confidence intervals for our parameters.

Bootstrap can be applied to regression models to give insights into variability of our parameters (beta) with minimal assumption about parent distribution. There are a couple ways that we can bootstrap a regression model: 

Parametric bootstrapping — resampling from all of the points (X):

1. Sample the data with replacement numerous times (100)
2. Fit a linear regression to each sample
3. Store the coefficients (intercept and slopes)
4. Plot a histogram of the parameters
5. Make inferences about true parameters

Non-parametric bootstrapping - resampling the residuals (Y):
- Implicit Assumption: errors are IID 

1. Find the optimal linear regression on all the original data
2. Extract the residuals from the fit
3. Create new y-values using the residual samples
4. Fit the linear regression with the new y-values
5. Store the slope and intercepts
6. Plot a histogram of the parameters
7. Make inferences about true parameters

*[Read](https://towardsdatascience.com/linear-regression-with-bootstrapping-4924c05d2a9) here for more examples.*

**Q5: Tell me why and how to apply bootstrapping on AB Testing?**

You can imagine you are data scientist in a gaming company, and you were assigned a AB Testing task.

Here is the Hypothesis: 

Where we should put the first gate? Level 30 vs. Level 40

After [python simulation](https://github.com/jazzsun10/bootstraping_code_demo), we get the result below.

First one is our Day 7 Retention bootstrap distribution by different version, you could see gate 30 day7 retention rate is higher than gate 40.

However, we don't know how much confidence we have to this conclusion.


![Day 7 Retention bootstrap distribution by different version](https://github.com/jazzsun10/bootstraping_final_project_demo/blob/main/Day%207%20Retention%20bootstrap%20distribution%20by%20different%20version.png)


As a result, we calculate the probability, it show us there is a 99.9% probability that 7-day retention is greater 
when the gate is at level 30.

![Day7 Rention rate difference between Gate 40 and Gate 30](https://github.com/jazzsun10/bootstraping_final_project_demo/blob/main/Day7%20Rention%20rate%20difference%20between%20Gate%2040%20and%20Gate%2030.png)


