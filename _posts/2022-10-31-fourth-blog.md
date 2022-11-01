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

We start with a simple linear regression model. Once we have selected all the available independent variables in the model, and fit it, the summary of the models are available in all the tools, where we can see the p-values of each IV. Depending on the confidence level (alpha), we can subset out the IVs that are statisically significant. All other non-significant variables can be removed from the model to make the model "better".


As we move to some more complex models, we have other models that provide the ability to select the best fitting IVs. Some of the models to note here are:

  * Backward Elimination
  * Forward Selection
  * Stepwise Forward
  * Stepwise Backward
  * Best Subset Selection
  * LASSO

(Some of the models are classified as the Criterion-based procedure models since they operate on basis of AIC and BIC values of the model. We'll talk about that in a while)

The backward elimination (BE) model and the Forward Selection (FS) models work on opposite concepts. The BE model takes the global model with all the IVs, and starts with eliminating the least significant IV, and reevaluate the model, while FS works with starting with most significant IV from the model, and adding one IV at a time and reevaluate the model. Out of the two, most practicing statisticians prefer the Backward Elimination model, especially when collinearity is present in the data set.
Here, when any of these models is built, we get the selection of the best combination of the IVs for the model.


Coming to the two models. Stepwise Forward and Stepwise Backward model, they also work on opposite priciples, and they utilize the steps mentioned in the above models. In Stepwise forward, the step is started with null model, and a FS step is performed. After theat, after each inclusion of IV, a BE step is performed. Repeating this, this model is repeated until there are no IVs to add/remove. In stewpwise backward model, the starting step is the global model with all the IVs present, and the BE and FS cycle is implemented like the previous model, until there are no IVs left to remove/add.

One of the most stand-out model is the best subset selection model. For k IVs in the data set, this method generates 2^k models having every possible combinations of the IVs, and the best model from those models is selected based on AIC and BIC score. AIC (Akaike Information Criterion) and BIC (Bayesian Information Criterion) are criterion that evaluates any model that is fitting the data. The higher the values of these criteria, the better the model is fitting the data. Infact, all of the abpve mentioned models also work on basis of the model's AIC and BIC values.

Lastly, LASSO model is used when the data is high dimensional (IVs > sample size). The LASSO method imposes a penalty on the sum of squares or log likelihood that is equal to the absolute sum of regression coefficients. This method however is not much preferred by many practicians since there is not enough evidence for the validation of the performance of this model's tests. Also, when Lasso model is built, the prediction from that model is dependent on the scale of the covariates, and hence the transformation is done "internally" for some regression models for some tools.

Some of the boosted trees, and MLR models use the f-score to sort the most significant and affecting IV. F-score, also known as feature score is a score generated by the model that depicts the impact value of a particular IV on the data and prediction.

## Verdict and Conclusion
Overall, the idea of transformation and best IVs set selection is to make the model better. With transformations, one can eliminate any skewness in the dataset, and make it to a particular distribution depending on the type of distribution required. The selection of variable is however done to make the model more robust and make it better fitting to the data and more accurate for prediction. Hence, when we have a data set with large number of IVs. it is safe to do the necessary transformation, and best variable selection using many available methods (few noted above) to reduce any noise in the data, avoid underfitting of the data and increase accuracy in prediction
