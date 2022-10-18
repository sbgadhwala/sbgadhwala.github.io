# Exploratory Data Analysis (EDA)

As a data scientist, one of the very first tasks when given a data is to understand the data. Lots of tools are available that provide the ability to perform data analysis; R, Python, SAS to nanme some. An inital go-through to understand the dimensionality and all the various variables is the first step towards Exploratory Data Analysis. However, EDA is a lot more than that. Being a data scientist, you whould have an indepth idea about the field you're working in, and hence an end target or aim for why the analysis has to be conducted should be clear. One can reach out to higher level managers to set the goals and expectations from the provided data.

## Steps Involved In EDA

EDA can be both `graphical` and `non graphical`. We'll explore both of them here in this blog.

Exploratory Data Analysis can be done on from a single variable in the data set to the whole data itself. Based on the type of variables we are dealing with, we can proceed accordingly. The most common starting point is the summary of the data, which provides us some general statistics like miminum value, maximum value, mean, etc about numeric data in the data set. Moving onto the next step, one of the important analysis would be to count the number of missing variables, and check possibility to fill them with either mean or median of the data, depending on distribution.

Understanding the type of each variable is impoartant, whether to classify the variable as **continous/discrete/categorical/binary** etc, becomes critical when performing EDA. The following process to undertand more about the data, is to simply plot it. A simple scatter plot made for any varibale is enough to convey any patterns that the variable is exhibiting. Similar scatter plots can be laid out for all variables. This would help in understanding any seasonalities trend in the data which is quite useful when performing time series analysis and prediction.

The catergorical variables are also of a huge help when it comes to plotting the difference and contribution in data of each variable with respect to the categorical variable(s). The count, using bar plots and histogram can be used to visualize the distribution of the data for any variables.

When we are interested in making any regression models, correlation value between variables comes handy. Most of the laanguages provide a simple one line command to plot and see the correaltion between any of the variables (can be two variables or a whole data frame). This is where heatmap takes the win. A heatmap can be plotted out which helps in easily underdstand the value of a number based on the color of the graph.

Lastly, as a part of data cleansing, the outliers in a few of the variables can be removed to help reduce the noise and improve accuracy when performing any regression. The outlier can come in many forms, some may just be missing values, or some may be extraordinary values that seem to be out of the range of 95th percentile of the data (depending on confidence levels). Different methods are present to detect the outlier from the dataset, including box plots and count bar plots.

## Types of Graphical Visualization

There are many plots that can be drawn out to represent different characteristics of the data. Some of them are:  
  *  [Bar Plot](https://www.geeksforgeeks.org/bar-plot-in-matplotlib/)
  *  [Scatter Plot](https://en.wikipedia.org/wiki/Scatter_plot)
  *  [Line PLot](https://jakevdp.github.io/PythonDataScienceHandbook/04.01-simple-line-plots.html)
  *  [Box Plot](https://en.wikipedia.org/wiki/Box_plot)
  *  [Histogram](https://en.wikipedia.org/wiki/Histogram)
  *  [Probability Density Function](https://en.wikipedia.org/wiki/Probability_density_function)
  *  [Cummulative Distribution Function](https://en.wikipedia.org/wiki/Cumulative_distribution_function)

A bar plot and a histogram are generally used to see distribution of the variables; can be count, can be some metric, and can also be categorized with respect to variables. Scatter plots and Line plots are generally used to see any patterns in the data and seasonality trends if any. Box plot is used to see the outliers in the dataset, and the mean and median of the variables in the data. Probability Density functions is plotted when we want to visualize variability in the data with respect to any number, for example, a normal distribution bell curve. Cummulative distribution function supplements the PDF, and helps visualize which percentile of data falls on which number.

## Conclusion

There are a lot of ways to summarize and visualize the data based on raw data, transformed data, grouped data and even missing data. What is the main goal of EDA has to be kept in mind and all the analysis should revolve around that, which plots to make, what data is necessary, what should be removed, are all a part of Exploratory Data Analysis.
