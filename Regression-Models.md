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

## Regression to the Mean

* If the corrletaion is 1 there is no regression to the mean

## Statistical Linear Regression Models

* A probabilistic model for linear regression: $Y_i = \beta_0 + \beta_1X_i + \epsilon_i$, where $\epsilon_i$ are assumed iid $N(0, \sigma^2)$, $E[Y_i|X_i=x_i] = \mu_i = \beta_0 + \beta_1x_i$, $Var[Y_i|X_i=x_i] = \sigma^2$, and $Y_i$ are independent $N(\mu_i, \sigma^2)$

* The least squares estimate is exactly the maximum likelihood estimate (regardless of $\sigma$)

* $\beta_0$: the expected value of the response when the predictor is 0 $E[Y|X=0]$

* $\beta_1$: the expected change in response for a 1 unit change in the predictor $E[Y|X=x+1] - E[Y|X=x]$

## Residuals and Residual Variation

* Residual: $e_i = Y_i - (\hat{\beta}_0 + \hat{\beta}_1X_i) = Y_i - \hat{Y}_i$

* Least squares minimizes $\sum_i e_i^2$

* Properties of the residuals: $E[e_i] = 0$, if an intercept is included, $\sum_i e_i = 0$, and if a regressor variable, $X_i$, is included in the model $\sum_i e_i X_i = 0$ 

* Residual plots highlight poor model fit

* The ML estimate of $\sigma^2$: $\frac{1}{n} \sum_i e_i^2$

* Total Variation = Residual Variation + Regression Variation:  $\sum_i (Y_i - \bar{Y})^2 = \sum_i (Y_i - \hat{Y}_i)^2 + \sum_i (\hat{Y}_i - \bar{Y})^2$

* The percentage of total variation described by the model: $R^2 = \frac{\sum_i (\hat{Y}_i - \bar{Y})^2}{\sum_i (Y_i - \bar{Y})^2} = 1 - \frac{\sum_i (Y_i - \hat{Y}_i)^2}{\sum_i (Y_i - \bar{Y})^2}$

* $R^2$ is the sample correlation squared

* $R^2$ can be a misleading summary of model fit
