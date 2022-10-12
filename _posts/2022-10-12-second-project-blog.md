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

The helper fuction for this API is such that it expects user to give Start Date and End Date as mandatory inputs, while, if the speed and half angle would take a default value of 0 if left blank.

Finally, the wrapper function that was created first which would allow the user to give the API name that they are intersted in as an input, along with the modifiactions for that endpoint that the user wants to select and modify. To access my defined API function, user can give either "CME" or "Coronal Mass Ejection (CME) Analysis as the input for API.
