# Introduction
## Background
In this final project I am going to discuss, analyze the data of restraunts in NEWYOKCITY, the aim of this project eventually is going to be segmenting the restraunts in NYC with corresponding traditional cuisines


## Problem 
- Do cluster analysis for all food related venues and find optimal locaation(s) for establishing new restraunt inn NYC ,using Foursquare api

I am taking the newyork city data set as given from assignment and making a model to cluster the data in such a way that we will be goin to have perfect idea on how different type restraunts are functioning well in their repective surroundings
so data of neighbours is taken from web and respectvive restraunts data is scraped using FOURSQUARE's places,venue api

## target audience/stakeholders
for a person who wants to open restraunt in NYC this project will be helpful in choosing place for his type of restraunt. Or this can also be focused for people who are planning for online food delivery startups. they can use this for opening new branches in optimal location(s) near to major restraunts 

# Data
## description of the data
source :  https://geo.nyu.edu/catalog/nyu_2451_34572
NYC has many neighbourhoods(nothing but major landmarks). the above source provide many such major neighbourhoods in NYC
here comes https://foursquare.com/ we use this for getting all venues within provided radius of all neighbouhoods
- we got 305 neighbours
- venues are taken from foursquare API
- This data may include offices, universities, crowded areas like theaters and parks in NYC
- data will have latitudes and longitues of such workplaces and we'll find optimum location in various clustered regions

## so data is
Country/City: NYC
Goal: Open a restaurant for  workers in weekdays
So, I will cross data from working days, and localisations.

### I will use the following API:
Foursquare API: to find restaurant/venues
### the neighbourhood data looks like this 
![neighbourhood](https://user-images.githubusercontent.com/68729609/125493624-22ae41c8-5e49-4ff1-bbe3-dcbf6f8397ee.png)
### single venue given by foursquare api would look like this
'''ymal
{'id': '4c783cef3badb1f7e4244b54',
  'name': 'Carvel Ice Cream',
  'location': {'address': '1006 E 233rd St',
   'lat': 40.890486685759605,
   'lng': -73.84856772568665,
   'labeledLatLngs': [{'label': 'display',
     'lat': 40.890486685759605,
     'lng': -73.84856772568665},
    {'label': 'entrance', 'lat': 40.890438, 'lng': -73.848559}],
   'distance': 483,
   'postalCode': '10466',
   'cc': 'US',
   'city': 'Bronx',
   'state': 'NY',
   'country': 'United States',
   'formattedAddress': ['1006 E 233rd St',
    'Bronx, NY 10466',
    'United States']},
  'categories': [{'id': '4bf58dd8d48988d1c9941735',
    'name': 'Ice Cream Shop',
    'pluralName': 'Ice Cream Shops',
    'shortName': 'Ice Cream',
    'icon': {'prefix': 'https://ss3.4sqi.net/img/categories_v2/food/icecream_',
     'suffix': '.png'},
    'primary': True}],
  'referralId': 'v-1626194459',
  'hasPerk': False}

'''
