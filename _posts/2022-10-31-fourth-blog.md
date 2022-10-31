# Variable Selection for Regression Models

While starting out on regresison, any statisticaian would have to go through the data set itself. For data sets having a large number independent variables, it not only becomes important but also a mandatory step to select the best variables for the regression model. Generally 10-30 independent variables are considered as "large amount" of IVs. Hence, to reduce noise in the data, reduce error in prediction, and to make the model better, the selection of the best IVs is a good practice to follow.

## Tranformations

Before we actually go to the variable selection step, variable transformation also helps most of the times. To see if we need to transform any independent variables or the dependent variable is by simply plotting them. Whem the variables are plotted, one can see the distribution of those values of the variables. For most cases a normal distribution is expected and counted as ideal condition. For the variables that don't follow that distribution can be transformed. Transfomrations can be of many types. Few are noted below:

  *  Log Transformation
  *  Box-Cox Transformation
  *  Arcsine Transformation

The most easiest one is the log transformation where we simply take the log of that variable and use it for furher modelling and analysis. Next up, box-cox transfomation is a little more dynamic than log, since it delas with the variance and mean of the data that has to transformed and it adjusts the Labmda accordingly. Lastly, arcsine transformation is used to transform that represents probability or proportions between 0 and 1. The arcsine transformation will help make the variances more constant throughout the data such that it would appear normally distributed as well. All these discussed transformations are readily available in almost any data science tools and languages (like R, Python and SAS to name some).

Note: If any variable is transformed, one has to transform it back to its original data distribution type either after designing the model or before making predictions using that model.

## Variable Selection

After we are done with transformations of the variables, lets have a little more look into how to select the "best" variables. The variable selection is also knows as finding the best combination of the original variables to include in a model.

We start with a simple linear regression model. 
