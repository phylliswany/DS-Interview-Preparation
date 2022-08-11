# Regression Models

Course Website: https://www.coursera.org/learn/regression-models

Slides: https://github.com/phylliswany/courses/tree/master/07_RegressionModels

Videos: https://www.youtube.com/playlist?list=PLpl-gQkQivXjqHAJd2t-J_One_fYE55tC

## Basics

* The empirical mean: $\bar{X} = \frac{1}{n} \sum_i X_i$

* The empirical variance: $S^2 = \frac{1}{n-1} \sum_i (X_i-\bar{X})^2$

* Normalization: $Z_i = \frac{X_i-\bar{X}}{S}$

* The empirical covariance: $Cov(X, Y) = \frac{1}{n-1} \sum_i (X_i-\bar{X})((Y_i-\bar{Y}))$

* Correlation: $Cor(X, Y) = \frac{Cov(X, Y)}{S_XS_Y}$

* $Cor(X, Y)$ measures the strength of the linear relationship, with stronger relationships as $Cor(X, Y)$ heads towards $-1$ or $1$

## Regression via Least Squares

* The least squares model: $Y = \hat{\beta}_0 + \hat{\beta}_1X$, where $\hat{\beta}_1 = Cor(X, Y)\frac{S_Y}{S_X}$ and $\hat{\beta}_0 = \bar{Y} - \hat{\beta}_1\bar{X}$ 

* The line passes through the point $(\bar{X}, \bar{Y})$

* If you normalized the data, $\hat{\beta}_1 = Cor(X, Y)$ and $\hat{\beta}_0 = 0$ 
