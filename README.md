# Analysis and Modelling of Urban Footfall Data in York City Centre

## Abstract
This repository presents an overview of one of my projects completed during my MSc at City University.<br>
In this project I look at footfall data from five distinct streets in the center of York (U.K.) <br>
collected as daily times series. This data is supplemented with weather (temperature and precipitation) <br>
and business occupancy time series as well as introducing auto-regressive features into the initial dataset <br>
to model and predict daily footfall for each each street. I compare and contrast random forests and <br>
regularised and non-regularised linear regression models on this augmented dataset.<br>


## Overview
![Camera Locations](https://raw.githubusercontent.com/AttitudeAdjuster/Analysis-and-Modelling-of-Urban-Footfall-Data-in-York-City-Centre/master/img/CamerasLoc.png)
Footfall data is automatically collected and calculated from street cameras in 5 distinct locations in the centre of York<br>
We want to analyse the data, correlate it with other data (weather, seasonality, and commercial venues occupancy rates) to see how precisely we can model it. <br>
We sourced the data from the following repositories:
* York City footfall from https://data.yorkopendata.org/ [1]
* York Business rates data available at same address
* York City weather data 
at https://weather.elec.york.ac.uk/data/vaisala/archives/ [2]

A similar project has been conducted at the University of Leeds.<br>
http://lida.leeds.ac.uk/news/project-update-predictive-data-analytics-for-urban-footfall/[3]<br>
The research looked at aggregate footfall data from Leeds city centre. One of the takeaway of the study was to emphasize <br>the key prominent explanatory variables: weather and day of the week. 
In this study, we are looking at a different dataset and we are considering each individual street separately, <br>not as a group of streets in similar locations.

## Problems and analytical questions
Compared to the Leeds’ study the challenges here are numerous:
* Sparsity of data: as we are looking at street level models, with less data samples overall per model.
* Noise: the data collection process can suffer from site-specific issues are not averaged-out by using multiple locations. Also, specific events occuring in a street can distort whatever patterns are present.
* Feature engineering: we might require additional features to correlate and compensate for the existing information deficit.
Some of the analytical questions we hope to answer are:
* Is there an identifiable intrinsic structure to the footfall dynamic for a given street? 
* How is footfall correlated to long lasting geographical structures (number of shops in street in our case)?
* How much auto-correlation in the time series is there due to the weekly cycle and are there long-term seasonality effects?
* How accurately can we fit a machine learning model to forecast footfall.<br>

## ETL and EDA
### Weather data
Raw data:
![Weather](https://raw.githubusercontent.com/AttitudeAdjuster/Analysis-and-Modelling-of-Urban-Footfall-Data-in-York-City-Centre/master/img/WeatherData%20Conso.png)

### Occupancy data
Raw data:
![Raw Occcupancy](https://raw.githubusercontent.com/AttitudeAdjuster/Analysis-and-Modelling-of-Urban-Footfall-Data-in-York-City-Centre/master/img/occupancy_example.png)

Occupancy Ratios as time series computed from raw data:
![Occupancy Ratio](https://raw.githubusercontent.com/AttitudeAdjuster/Analysis-and-Modelling-of-Urban-Footfall-Data-in-York-City-Centre/master/img/OccupancyData.png)

### Footfall data
Time serie visualisation:
![TS](https://raw.githubusercontent.com/AttitudeAdjuster/Analysis-and-Modelling-of-Urban-Footfall-Data-in-York-City-Centre/master/img/FootfallMay2017.png)

K_means clustering to reveal weekly dynamics per street:
![Week Clusters](https://raw.githubusercontent.com/AttitudeAdjuster/Analysis-and-Modelling-of-Urban-Footfall-Data-in-York-City-Centre/master/img/week_clusters.png)

Week-on-week autocorrelation plots:
![Auto correl](https://raw.githubusercontent.com/AttitudeAdjuster/Analysis-and-Modelling-of-Urban-Footfall-Data-in-York-City-Centre/master/img/Autocorrelone.png)

Yearly patterns:
![Yearly](https://raw.githubusercontent.com/AttitudeAdjuster/Analysis-and-Modelling-of-Urban-Footfall-Data-in-York-City-Centre/master/img/polar_yearly.png)











