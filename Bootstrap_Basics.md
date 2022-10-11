## 3 Levels of Explanation of Bootstrapping

### Level 1. <br>
Bootstrapping is a method in statistics that allows us to estimate things we are interested to know using a sample dataset. Let's say we are interested in learning about baby birth weights, and we can only obtain one sample of 100 baby weights due to resource constraints. In this case, using bootstrapping can help us make inference about the all the baby birth weights (our population) without requiring us knowing anything about the population. Overall, bootstrapping is a very helpful technique in data science and modeling to produce a number of resamples from a single sample dataset so that we can use to do further statistical tests or analysis.

### Level 2. <br>
Bootstrapping is a statistical method for estimating properties, such as standard errors and confidence interval, of a given statistics, such as mean or median. And the way it estimates the statistics is by using the observed sample data that we have to simulate a number of resamplings from the population.

Here is a example to help explain the concept. Say we're interested in learning about the mean and confidence interval of the baby weights. We have an iid sample of baby birth weights of size n=100 with mean u. Bootstrapping allows us to use this sample data to create new samples, by random select another 100 data from our original sample WITH REPLACEMENT, meaning one sample can be picked multiple times. This would result in a new sample of 100, and a new sample mean. We then repeat these steps a large number of (k) times to get k new sample means, which we then construct a bootstrap distribution, a approximation of sampling distribution, which we can calculate different properties such as standard deviation or confidence interval.

Overall, bootstrapping is a resampling technique, that allows us to estimates properties of any statistics, not just mean, which can be comes in very helpful when parametric inference is impossible.

### Level 3. <br>
Bootstrapping is a statistical method that uses the observed data to simulate resamplings from the population, which we calculate a statistic each time, and use the dstribution of the simulated statistic to approximate characteritics of the population. In other words, in bootstrapping, our observed data becomes the population, and we get samples from that population. There are also different types of bootstrap scheme including bayesian bootstrap, smooth bootstrap or parametric bootstrap that we can use accordingly.

Bootstrapping can come in handy when the pouplation distribution is unknown and our traditional parametric inferenece methods won't apply well. Another advantage of bootstrapping is it allows us a simple way to construct properties of a statistics even when the formal way of calculating such properties is complex. One disadvantage of bootstrapping is that is depends heavily on the estimator we used and we will not always yield asymptotically valid results.

Overall, bootstrapping is a great resampling technique to add to our toolbox and can be very helpful in certain sceanarios in modeling or inference.
