# Statistical Inference

Course Website: https://www.coursera.org/learn/statistical-inference

## Probability

* For any two events the probability that at least one occurs is the sum of their probabilities minus their intersection:
$P(A_1 \cup A_2) = P(A_1) + P(A_2) - P(A_1 \cap A_2)$

* PMF: A probability mass function evaluated at a value corresponds to the probability that a random variable takes that value.

* PDF: A probability density function, a a function associated with a continuous random variable. Areas under PDFs correspond to probabilities for that random variable.

* The cumulative distribution function (CDF):
$F(x) = P(X \leq x)$


* The survival function:
$S(x) = P(X \geq x) = 1 - F(x)$

* The $\alpha^{th}$ quantile of a distribution with distribution function $F$ is the point $x_{\alpha}$ so that $F(x_{\alpha}) = \alpha$

* A percentile is simply a quantile with $\alpha$ expressed as a percent.

* Estimand: the population median

* Estimator: the sample median

## Conditional Probability

* The conditional probability of an event $A$ given that $B$ has occurred: 
$P(A|B) = \frac{P(A \cap B)}{P(B)}$

* If $A$ and $B$ are independent:
$P(A|B) = \frac{P(A)P(B)}{P(B)} = P(A)$

* Bayes' rule: 
$P(B|A) = \frac{P(A|B)P(B)}{P(A|B)P(B) + P(A|B^c)P(B^c)}$

* Two events $A$ and $B$ are independent if:
$P(A \cap B) = P(A)P(B)$

* If $A$ is indepdent of $B$, then $A^c$ and $B^c$

* Random variables are said to be iid if they are indepedent (statistically unrelated from one and another) and identically distributed (all having been drawn from the same population distribution)
