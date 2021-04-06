---
layout: post
title: "Logistic Regression & Post-Stratification Analysis to Predict the Results of the 2020 American Election"
date: 2020-11-02
---

We are interested in predicting the popular vote outcome of the 2020 American federal election with
individual-level public opinion survey data from the Democracy Fund + UCLA Nationscape and the 2018
5-year American Community Survey (ACS) census data from IPUMS USA (Ruggles et al., 2020; Tausanovitch
& Vavreck, 2020). We will conduct regression analysis on the survey data to estimate the voter response, and
select demographic variables from the census data to conduct a post-stratification analysis and estimate the
voting results of the American population. In the following analysis, we will construct two logistic regression
models–one to estimate the vote response for Donald Trump, the other to estimate the vote response for Joe
Biden–and perform the post-stratification calculations.

The interpretation of each estimate will follow the same principles. For example, with significance of variables
in this analysis determined by the p-value threshold of p < 0.05, it can be seen in Figure 1 that the age30-44
group is significant and has an estimate of beta1 = 0.6562082. The regression estimates are the log odds of the
voting estimate, therefore the interpretation of this result is that the likelihood of voting for Trump in the
age30-44 group is exp(beta) = 1.9274699 times that of voting for Trump in the age18-29 group, when controlling
for all other variables.

For the model estimating the proportion of voters voting for Trump, the following variable categories are
significant: age30-44, age45-64, age65+, Black or African American, Chinese, Other race or two or more
races, Male, and South.

For the model estimating the proportion of voters voting for Biden, the following variable categories are
significant: age30-44, age45-64, Black or African American, Chinese, Japanese, Other Asian or Pacific Islander,
Other race or two or more races, Male, and South.
Interestingly, none of the education level categories were significant compared to 3rd Grade or less education
in both of the models.

We corrected the log odds from the logistic estimation in the post-stratification calculations, and calculated
the proportions of votes that the two candidates are each likely to receive. y1 for Trump is 0.4181068, and y2
for Biden is 0.4441705. These results indicate that ~41.81% of voters are willing to vote for Trump, while
another ~44.42% of voters prefer to vote for Biden. The two values do not add up to 100% because as
mentioned above, some respondents either indicated that they would not vote, or did not yet know how they
would vote. Our results predict that Joe Biden will gain more votes in total compared to Trump.
