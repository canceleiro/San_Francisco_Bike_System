# San Francisco bike sharing system
## by Javier Alonso Alonso

## Installations required

> My project contains a jupyter notebook, so that´s the only necessary software you´d need. Be sure to have installed on in numpy, pandas,  matplotlib and seaborn

## Project motivation

> My data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area

> My motivation is try to see how the different users of the system (subscribers and customers) use the bycicles, analyzing the number of trips and duration of them depending on hour, day of the week and month of the trip

## File descriptions

> The files in this project are:

>- readme.md: describes the project and motivations of it

>- San_Francisco_bikes_Analysis.ipynb: Jupyter Notebook where all the work is done, including data wrangling and exploration

>- CSV data files: the files with data of the bike rides downloaded from https://s3.amazonaws.com/baywheels-data/index.html

## Interactions with the project

> The user must run the jupyter notebook that does the next main steps:

>- Gathering Data
>- Asessing and cleaning Data
>- Consolidation of dataframes to files
>- Univariate Exploration
>- Bivariate Exploration
>- Multivariate Exploration
>- Final conclussions



### Dataset

> The main dataframe (df_trips) contains all the trips made on the bike sharing system of San Francisco and after all the wrangling issues have the next fields:

> - start_time: when the trip began
> - start_station_id: the identifier of the station where the trip begins
> - end_station_id: the identifier of the station where the trip ends
> - bike_id: the identifier of the bike used on the trip
> - user_type: if the user of the bike is a Subscriber or a Customer
> - duration_min: the duration of the trip in minutes
> - date: the day, month and year when the trip begins
> - hour: the hour where the trip begins
> - month: the month where the trip begins
> - day_week: the day of the week when the trip begins, being 1 Monday, 2 Tuesday,... until 7 Sunday

> There´s also an auxiliary dataframe (df_stations) that contain information of the bike stations, having the next fields:

> - id: identifier of the station, related to the id´s of the start and end station of the main dataframe
> - name: name of the station
> - latitude: latitude of the station
> - longitude: longitude of the station

> To get this final dataframes have been many wrangling issues (gathering, assesing and cleaning) that are explained in detail in "exploration_template.ipynb"

> Once made the wrangling issues the observatory actions were made, begining with univariate analysis to multivariate in the next step.

## Summary of Findings

> There are two types of users, subscribers and customers. Subscribers are recurrent users that use the bike on a daily basis, most of them San Francisco citizens, and customers are sporadic users, most of them tourists. Both type of users behave differently using the bikesharing system.

> The duration of the tourists trips are much longer than the ones of the citizens because they use the bike for tourism and for travelling around the city, while the subscribers use it for going to one place to other directly, and during the non weekend days the majority of the trips are from home to job or viceversa. In both cases the duration of the the trips are quite longer during weekends.

> The duration of trips depending on the hour is quite constant for the subscribers, as their trips are usually between near places of the city all along the day. On the other hand, in the case of customers the duration is higher during the sunny hours of the day as they use it for visiting different places of the city and don´t release the bikes on the station. During night in both cases there´s a peak around 3 in the morning due to the closing time of bars and discos and they come back to hotel or home. 

> The number of trips taken by subscribers and costumers vary a lot, beeing much higher the trips of the citizens along the year. The number of trips for customers is almost constant during the seven years of the week because the number of tourists don´t vary too much between days. On the other hand the trips of subscribers descend a lot during weekends because most of the trips out of the weekend are due to the transport between job and home and viceversa

> During the two years per month the subscribers trips are always higher than the costumers but both behave in a similar way, being greater in the middle months of the year and being lower in winter, except from last month analyzed, December 2019, were both have similar number of trips due to a high descend in citizens trips and a high uprise in tourist trips. Probably there´s a reason for this abnomal behaviour.

> Looking at the hour of the trip, the peak hours are at the time going to work (7-8AM) and coming back (17-18h)
