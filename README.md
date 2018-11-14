# Analysis and Modelling of Urban Footfall Data in York City Centre

### Abstract
This repository presents one of my projects completed during my MSc at City University.<br>
In this project I look at footfall data from five distinct streets in the center of York (U.K.) <br>
collected as daily times series. This data is supplemented with weather (temperature and precipitation) <br>
and business occupancy time series as well as introducing auto-regressive features into the initial dataset <br>
to model and predict daily footfall for each each street. I compare and contrast random forests and <br>
regularised and non-regularised linear regression models on this augmented dataset.<br>


## Overview
![Camera Locations](https://raw.githubusercontent.com/AttitudeAdjuster/Analysis-and-Modelling-of-Urban-Footfall-Data-in-York-City-Centre/master/img/CamerasLoc.png)
Footfall data is automatically collected and calculated from street cameras in 5 distinct locations in the centre of York<br>
We want to analyse the data, correlate it with other data (weather, seasonality, and commercial venues occupancy rates) to see<br> how precisely we can model it. <br>
We sourced the data from the following repositories:
* York City footfall from https://data.yorkopendata.org/ [1]
* York Business rates data available at same address
* York City weather data 
at https://weather.elec.york.ac.uk/data/vaisala/archives/ [2]

A similar project has been conducted at the University of Leeds.<br>
http://lida.leeds.ac.uk/news/project-update-predictive-data-analytics-for-urban-footfall/[3]<br>
The research looked at aggregate footfall data from Leeds city centre. One of the takeaway of the study was to emphasize <br>the key prominent explanatory variables: weather and day of the week. 
In this study, we are looking at a different dataset and we are considering each individual street separately, <br>not as a group of streets in similar locations.





