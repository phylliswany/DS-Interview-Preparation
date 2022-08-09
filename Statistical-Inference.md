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
