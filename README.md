# Project Name
> Multiple linear regression model for predicting demand of shared bikes


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- This assignment is a programming assignment wherein we built a multiple linear regression model for the prediction of demand for shared bikes.
- Background: A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.
- Business Problem: BoomBikes wants to know the drivers affecting the demand of shared bikes so that they could understand and cater to the people's needs to increase their profits. So we need to find the factors using multiple linear regression affecting the demand so that company could take necessary adjustments and actions to increase their profits.
- Dataset: day.csv have the following fields:
	
	- instant: record index
	- dteday : date
	- season : season (1:spring, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2018, 1:2019)
	- mnth : month ( 1 to 12)
	- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : temperature in Celsius
	- atemp: feeling temperature in Celsius
	- hum: humidity
	- windspeed: wind speed
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- temperature is the most important driving factor behing the demand of shared bikes. One unit change in temperature increases the demand by approx 5195 units if other drivers are kept constant
- Light rain is a negative driving factor. A day with light rain decreases the demand by approx 2015 units if other drivers are kept constant
- When the calendar year changed from 2018 to 2019, the demand suddenly increases by approx 1981 units if other drivers are assumed unchanged
- Similarly if the month is september, of if the season is summer or winter - all these factors increases the demand of shared bikes
- windspeed, humidity, cloudy weather, holiday, the month of July, or light rain as mentioned above, decreases the demand of shared bikes.
- Model:  cnt = 1988.33 + 1981.38yr - 859.72holiday + 5195.64temp - 1500.5hum - 1646.97windspeed + 708.65summer + 1170.77winter -436.27Cloudy -2015.06Light Rain -415.6July + 835.94September
- Adjusted R2 score on training set : 0.84, r2 score on test set: 0.805

## Technologies Used
- Python - version 3.9.12
- numpy - version 1.21.5
- pandas - version 1.4.2
- matplotlib - version 3.5.1
- seaborn - version 0.11.2
- scikit learn 1.0.2
- statsmodels 0.13.2


<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This project was done as part of assignment


## Contact
Created by @IamVib - feel free to contact me!
