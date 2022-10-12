# Project 2 - NASA APIs

I finished my [second project](https://sbgadhwala.github.io/ST558_Project2/) for the ST558: Data Science for Statisticians course that revolved around dealing with APIs and Exploratory Data Analysis. The main aim of this project was to get a hands on experience with different API endpoints, and all the different modifications that the endpoint offers.  In this project, I worked with one of [NASA APIs](https://api.nasa.gov/index.html) for space weather science - [Cornonal Mass Ejection (CME) Analysis](https://api.nasa.gov/index.html#donkiCMEAnalysis), which is an API that helps fetch the collected data for all the cornoal mass ejection events that occurred on the sun's corona layer.

To start with the API itself, I used multiple packages listed below:
 * httr
 * jsonlite
 * tidyverse
 * ggplot2
 
 
First, I explored the NASA's website to know all the details about this API. The Coronal Mass Ejection (CME) Analysis API endpoint has a total of 8 modifications, out of which I used 4. They are:
  * Start Date (startDate)
  * End Date (endDate)
  * Speed (speed)
  * Half Angle (halfAngle)

The helper fuction for this API is such that it expects user to give Start Date and End Date as mandatory inputs, while, if the speed and half angle would take a default value of 0 if left blank. For the given start date, end date, speed and half angle, a target URL would be generated and called, and that API call would return JSON formatted data of all the CME events that occured between those dates and had those speed and half angle characteristics.

One of the most challenging part of the API function call was to:
 * Understand the structure of the data, and see which information is at which level, extract the important and relevant information and put them into a tibble collectively and return that from the function 
 * To understand what data is relevant and what can be ignored. After a thorough observation through the data, the following details regarding the events was returned in for of a tibble:
   * Time (of the CME event)
   * Latitude (of the CME event)
   * Longitude (of the CME event)
   * Speed (of the explosion)
   * Half Angle (of the explosion)

To understand more about the data retrieved from the API, I performed some Exploratory Data Analysis (EDA), and created relevant graphs using the ggplot2 library. One of the main challenges in that was to:
  * decide which varibales to plot
  * How to communicate the data details effectively
 
 For this, I created my own varibales from the existing variables in th data, and plotted several graphs usign them, and one of the most intersting graph I plotted is the one that depicts the latitude and longitude of the sun where each CME event took place, classified according to their event type and speed. That graph is as shown:
 

Finally, the wrapper function that was created first which would allow the user to give the API name that they are intersted in as an input, along with the modifiactions for that endpoint that the user wants to select and modify. To access my defined API function, user can give either "CME" or "Coronal Mass Ejection (CME) Analysis as the input for API.
