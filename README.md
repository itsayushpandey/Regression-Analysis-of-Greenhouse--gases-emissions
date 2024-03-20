# Regression-Analysis-of-Greenhouse--gases-emissions

# Research Paper : https://journals.tubitak.gov.tr/cgi/viewcontent.cgi?article=1505&context=elektrik

## Introduction
### Monitoring the greenhouse gas emissions can be a time and resource consuming task for a lot of the industries. Both periodic measurements and continuous emission monitoring systems can be cost intensive as they would require constant monitoring of the sensors used to measure the gas emissions. Research was published by the Turkish journal of Electrical and Computer Science department to tackle this issue. The research proposes a predictive emission monitoring system (PEM) that predicts the emissions of CO and NOx using calibrated equipment established on site. The researchers set a benchmark for the predictive models built and this project is an attempt to apply statistical methods for the data


## Linear Model for CO Emissions:

The initial approach involves fitting a linear regression model using all available predictors. However, this model encounters violations of assumptions such as normality, linearity, and homoscedasticity.
Diagnostic plots reveal these issues, particularly the fitted vs. actual plot indicating a non-linear relationship.
To address this, a transformation is applied to the response variable (CO emissions) to achieve linearity. The square root transformation is chosen, resulting in a more linear relationship.
Weighted least squares (WLS) regression is then employed to handle heteroscedasticity, with weights estimated based on the variance of the transformed response variable across different levels of a predictor (Turbine energy yield, TEY).
Model selection techniques, including feature subset selection using regsubsets, are utilized to identify a subset of predictors that minimizes the residual sum of squares (RSS) while maintaining model interpretability.
Ridge regression is explored as a method to address multicollinearity among predictors by penalizing coefficients. However, in this case, the impact is minimal due to already low parameter estimates.


## Linear Model for NOx Emissions:

Similar to the CO modeling approach, initial attempts involve fitting a linear regression model using all predictors. However, it is found that one predictor (Gas turbine exhaust pressure, GTEP) is insignificant.
Diagnostic plots reveal violations of assumptions, particularly non-normality and non-linearity.
To address these issues, a log transformation is applied to the response variable (NOx emissions), resulting in a more linear relationship.
Model selection techniques, similar to those used for CO modeling, are employed to identify a subset of predictors that minimize RSS.
Attempts to use ridge regression to address multicollinearity among predictors show limited impact due to low parameter estimates.


## Evaluation and Results:

Various performance metrics, such as adjusted R-squared, mean absolute error (MAE), and mean squared prediction error (MSPE), are used to evaluate the performance of different models for both CO and NOx emissions.
Comparison of models, including linear models with transformations, weighted least squares, and ridge regression, is presented to determine the most effective approach for predicting emissions.

## Summary
The regression modeling part of the paper involves iterative steps to address violations of assumptions, multicollinearity, and model complexity, ultimately aiming to develop accurate and interpretable predictive models for CO and NOx emissions from the gas turbine.

## Conclusion
Through this paper we test the statistical significance of a predictive emission monitoring system (PEM). The paper we based this research on did sophisticated neural networks. Considering we achieved comparable results with statistical modeling which is more interpretable and explainable would mean that the 9 features used can very well be used to set up a PEM. There could be more uses to this model like building confidence intervals for each predictors to set up triggers when the emissions exceed the limit set up.
