# Statistical Inference

Course Website: https://www.coursera.org/learn/statistical-inference

Slides: https://www.youtube.com/playlist?list=PLpl-gQkQivXiBmGyzLrUjzsblmQsLtkzJ

Videos: https://www.youtube.com/playlist?list=PLpl-gQkQivXiBmGyzLrUjzsblmQsLtkzJ

## Introduction

* Statistical inference is to infer facts about a population using noisy statistical data when uncertainty must be accounted for. 

## Probability

* For any two events the probability that at least one occurs is: $P(A \cup B) = P(A) + P(B) - P(AB)$

* The cumulative distribution function (CDF): $F(x) = P(X \leq x)$

* The survival function: $S(x) = P(X \geq x) = 1 - F(x)$

* The $\alpha^{th}$ quantile of a distribution with distribution function $F$ is the point $x_{\alpha}$ so that $F(x_{\alpha}) = \alpha$

## Conditional Probability

* Bayes' rule: $P(B|A) = \frac{P(A|B)P(B)}{P(A|B)P(B) + P(A|B^c)P(B^c)}$

* Two events $A$ and $B$ are independent if: $P(A \cap B) = P(A)P(B)$

* Random variables are said to be iid if they are indepedent (statistically unrelated from one and another) and identically distributed (all having been drawn from the same population distribution)

## Expected Values

* Our sample expected values (the sample mean and variance) will estimate the population versions



* Linearity of expectation: $E[\sum_{i=1}X_i] = \sum_{i=1}E[X_i]$

## The Variance

* The population variance: $Var(X) = E[(X - \mu)^2] = E[X^2] - E[X]^2$

* The sample variance is also a random variable: $S^2 = \frac{\sum_{i=1}(X_i - \bar{X})^2}{n-1}$

* The average of random sample from a population is itself a random variable: $E[\bar{X}] = \mu$ and $Var[\bar{X}] = \sigma^2 / n$

* The standard deviation $S$: how variable the population is

* The standard error $S/\sqrt{n}$: how variable averages of random samples of size $n$ from the population are

## Common Distributions

* The Bernoulli distribution: $P(X = x) = p^x(1-p)^{1-x}$, $E[X] = p$, $Var(X) = p(1-p)$

* The binomial mass function: $P(X = x) = \binom{n}{x}p^x(1-p)^{n-x}$

* The normal distribution: $f(x) = (2\pi\sigma^2)^{-1/2}e^{-(x-\mu)^2/2\sigma^2}$, $E[X] = \mu$, $Var(X) = \sigma^2$

* The Poisson distribution:  $P(X = x; \lambda) = \frac{\lambda^xe^{-\lambda}}{x!}$, $E[X] = \lambda$, $Var(X) = \lambda$

## Asymptotics

* Law of Large Numbers (LLN): the average of iid samples converge to the population means that they are estimating

* The Central Limit Theorem (CLT): the distribution of average of iid variables (properly normalized) becomes that of a standard normal as the sample size increases

* Confidence intervals: the quantity $\bar{X} \pm 2\sigma/\sqrt{n}$ is called a $95$% interval for $\mu$

* The Poisson and binomial case have exact intervals that don't require the CLT

## T Confidence Intervals

* T Confidence interval: $\bar{X} \pm t_{n-1}S/\sqrt{n}$

* The confidence interval for $\mu_y - \mu_x$: $\bar{Y}-\bar{X}\pm t_{n_x+n_y-2, 1-\alpha/2}S_p(\frac{1}{n_x}+\frac{1}{n_y})^{1/2}$

* The pooled variance estimator: $S_p^2 = ((n_x-1)S_x^2+(n_y-1)S_y^2)/(n_x+n_y-2)$

* Under unequal variances: $\bar{Y}-\bar{X}\pm t_{df} \times (\frac{s_x^2}{n_x}+\frac{s_y^2}{n_y})^{1/2}$, $df = \frac{(S_x^2/n_x+S_y^2/n_y)^2}{(\frac{s_x^2}{n_x})^2/(n_x-1)+(\frac{s_y^2}{n_y})^2/(n_y-1)}$

## Hypothesis Testing

* $\alpha$ = Type I error rate = Probability of rejecting the null hypothesis when, in fact, the null hypothesis is correct

* The $Z$ test for $H_0: \mu=\mu_0$ versus $H_1: \mu<\mu_0$, $H_2: \mu \neq \mu_0$, $H_3: \mu>\mu_0$

* Test statistic: $TS=\frac{\bar{X}-\mu_0}{S/\sqrt{n}}$

* Reject the null hypothesis when: $TS \leq Z_\alpha = -Z_{1-\alpha}$, $|TS| \geq Z_{1-\alpha/2}$, $TS \geq Z_{1-\alpha}$

## P-values

* P-value: the probability under the null hypothesis of obtaining evidence as extreme or more extreme than would be observed by chance alone

* The attained significance level: the smallest value for alpha that you still reject the null hypothesis

* For two sides hypothesis test, double the smaller of the two one sided hypothesis test Pvalues

## Power

* Power: the probability of rejecting the null hypothesis when it is false

* $\beta$ = Type I error rate = Probability of failing to reject the null hyppothesis when it's false

* When testing $H_a: \mu > \mu_0$, $1 - \beta = P(\bar{X} > \mu_0 + z_{1-\alpha}\frac{\sigma}{\sqrt{n}}; \mu=\mu_\alpha)$

* Power only needs $\frac{\sqrt{n}(\mu_\alpha-\mu_0)}{\sigma}$
