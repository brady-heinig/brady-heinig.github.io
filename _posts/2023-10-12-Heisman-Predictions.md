---
layout: post
title: "Using Multiple Linear Regression Methods to Analyze NBA Salary Disparity"
author: Brady Heinig
description: "Is your favorite player being overpaid or undervalued?"
image: /assets/images/sexton.jpg
---
## How do we assess if NBA players are being overpaid, underpaid, or properly compensated for their value on the court?


The NBA is one of the most watched sports leagues in the entire world, and there are thousands of NBA players who have made comfortable livings for their families and for generations to come thanks to the generous salaries they earn. When a player is excelling during the season and has yet to finish his rookie contract, fans praise him for being undervalued. If a player who just signed a max contract is going through a slump, people are quick to call him a fraud and claim he is overpaid. But what really determines what a player is financially worth, and how do we discover it? By walking you through building and analyzing a regression model, we will look to discover which players are truly playing beyond their contracts and which players are robbing their owner's bank accounts in broad daylight.


Source code for the project if you want to follow along can be found here (insert link)
### **Load in the Data**
- The data we are using comes from an NBA dataset found publically on kaggle here insert link.
- The dataset includes every player who logged a minute in an NBA game this year, and it includes all basic stats including points per game,     rebounds per game, assists per game, etc. Advanced stats are also included for each player.
```
{% raw %}![Figure]({{site.url}}/{{site.baseurl}}/assets/images/dataset.png){% endraw %}
```
### **Define our Variables**
- In multiple linear regression, you need to have more than one independent variables. In this study, we will be using several to explain our response variable 'Salary'.
### **Check Assumptions**
- For MLR, there are 4 assumptions that our data needs to meet in order for our model to accurately predict:
  - Linearity: Dependent and independent variable relationships should be linear.
  - Homoscedasticity: Variance of the errors should be constant.
  - Multivariate normality: The residuals need to be normally distributed.
  - Multicollinearity: There should be little or no multicollinearity in the data.
- For the sake of time, all the assumptions are met, refer to source code to see how to check assumptions for MLR
- Because assumptions are met, we are able to move on to our model testing and training
### **Test, Train, and Fit the Model**
- We will be using the scikit-learn library to help us in constructing our model, as well as matplotlib in order to perform some visualizations.
- We split our NBA data into two datasets: 80% train and 20% test
- Once the model is fit using player stats and salaries from the training set, we then use it to predict player salaries for the test data set.
- The plot below shows the difference between actual player salaries from the test dataset and the predicted values that our model gave us.
- Player salaries are easier for the model to predict because there are many more players who make average salaries in the NBA than those who make max salaries.
- As the player salaries get larger, the actual salary values become much larger than the predicted ones.
### **Analyze**
## Call to Action
