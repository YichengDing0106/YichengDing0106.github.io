---
layout: post
title: "What will affect the combined systolic blood pressure reading? A study of American over 17"
date: 2020-06-24
---

Nowadays, people are living under stress and health becomes a big problem. More
and more people start to worry about whether their blood pressure is within the
normal range. The purpose of this study is to find what factors will affect the
combined systolic blood pressure reading. Basically, we want to know the effect of
smoking on the combined systolic blood pressure reading and other factors that will
most affect the combined systolic blood pressure reading. After finding the
relationship between all the factors and the combined systolic blood pressure reading,
we can predict our combined systolic blood pressure reading more accurately and take
appropriate measures to improve our health.

This analysis was conducted using data collected by the US National Center for
Health Statistics which has conducted a series of health and nutrition surveys since
the early 1960s. About 5000 individuals were interviewed every year and complete
the health examination component of the survey since 1999. We selected the data
from American over 17. In the dataset, we have 17 variables that may be associated
with the combined systolic blood pressure reading.


Method

First, I fitted a multiple linear regression with all 17 variables. We need to know how
many observations have the potential to influence the position of the regression line,
so I did the model diagnostics in order to find the leverage points, cook’s distance,
and standard residual. We need to know how After that, I checked the variance
inflation factor to find which variables’ multicollinearities are high.

The next step is to do the variable selections. The purpose of doing the variable
selections is to get a better model. When there are too many predictor variables in the
model, the prediction variance will be very large. Moreover, fewer variables will help
us to better interpret the models. We want to neither overfit nor underfit the model, so
we need to select which variables we should consider in the model. I did the stepwise
selection with both AIC and BIC. With the variable selections results, I fitted two new
multiple linear models. And I also check the prediction error for both of them. Next, I
do the shrinkage methods to shrink some parameter estimates to zero by applying
some penalty or constraint. I fitted the ridge penalty and LASSO penalty to get two
new models. I checked the prediction error as well.

Last but not the least, we need to do the model validation. The reason for that is one
independent test is not enough to validate
a model, so we need to use the validation
set to validate the model. The method I
used is cross validation. I just randomly
split the data into 10 parts and fit the
model with 9 parts to predict the outcomes
for the remaining part. I did the cross
validation for both AIC and BIC. From the
graph, we can notice that the model with
BIC is more accurate than the model with
AIC.


Result

After fitting the multiple linear regression with all 17 variables, it seems no
relationship between all these variables
and the combined systolic blood pressure
reading. I found 11 leverage point and 0
point is influential based on Cook’s
distance. There are 98 observations that
are influential based on DEFFITS and 48
observations are influential based on
DEBETAS. And for the standardized
residual plot, it indicates that there is
some non-linearity between the response
and the predictors. After checking the VIF, I
found that the multicollinearities of weight
and BMI are high.

In order to get a better model, I did the variable selections with both AIC and BIC.
After doing the stepwise selection with AIC, I got the selected variables: Gender, Age,
Marital Status, Weight, Height, and BMI. For BIC, I got the selected variables:
Gender, Age, Weight, Height, and BMI. After doing variable selections and shrinkage
methods, I compare the prediction error of all the models. I find that the model of
stepwise selection with BIC has the smallest predict error.

In order to further get a better model, I
did the response vs fitted plot for the
model of stepwise selection with BIC.
And we can find that it seems the
response has a quadratic relationship
with the predictor. So, we need to apply
a square root transformation to get a
better model.


Discussion

Results from this study indicated that on average, the gender difference has the
greatest impact on the combined systolic blood pressure reading. BMI also has a great
impact on the combined systolic blood pressure reading. For one increase in BMI, on
average there is a decrease of 0.16% combined systolic blood pressure reading when
other variables are fixed at a constant value. The P-value of age is very small which
means age is very meaningful for this model. After fitting the model, we find that the
effect of smoking on the combined systolic blood pressure reading is not decisive. To
get the best range of the combined systolic blood pressure reading, we need to focus
more on BMI. We should control our BMI at a normal range. Both underweight and
overweight will adversely affect our combined systolic blood pressure reading.

This final model is not perfect. The variance inflation factor of BMI and weight is
high, which will cause high multicollinearity. In this model, we did not consider the
multicollinearity of BMI and weight, so the result will be a little bit offset. Since we
decrease the quantities of the variables to get a better interpretable model, we must
sacrifice some prediction accuracy. We cannot take into account both prediction
accuracy and an easier interpretable model. For a better-fitted model, we need
stronger data analysis skills.
