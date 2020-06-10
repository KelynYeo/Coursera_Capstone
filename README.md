# Coursera_Capstone
Coursera Capstone Project - The Battle of Neighborhoods
## 1. Introduction
As a part of the final IBM Capstone Project, we get a feel of what data scientists go through in real life. Objectives of the final assignments were to define a business problem, look for data in the web and, use Foursquare location data to solve or execute the problem.
### Problem Statement : Staying Safe while Travelling in a Foreign Country
### Background
So a little about myself, is that I **LOVE** to travel. However, travelling to another country requires so much planning. There are hundreds, or even thousands of different sites that I can do my research on to know about the most worth it accommodations, the must try food and sightseeing places. If I want to find out about all these places, well, I will at least need months of preparation. However, with my mind all occupied on where to go, I might just miss out on one of the most important information. 

*How prepared must I be in a foreign country?* These tourist areas might be surrounded with crime such as muggings, thefts or even assault. Going to these tourist venues might put my life in danger instead.
### Target Audience
This solution would be for *travellers* who wants to stay safe while having fun travelling in the country. This solution might even be applicable for people who are *moving to a new neighbourhood* and wants to know the vicinity a little better, to be prepared. 
## 2. Data 
### Data Description
In this section I will describe the data that is going to be used to solve the problem. I would be using **Toronto, Canada** as the example of the foreign country these target audience would be going. These target audience would be travelling to popular sites. We will then find out if they need to be prepared before heading to those areas.

The following data would be what I am going to use:
1.	Neighborhood in Toronto to find the most common veneue 
2.	User Foursquare API to get most common venue data
3.	Use Toronto Police Service Public Safety Data Portal to get crime data

### Data Prepration
#### a. Scraping Toronto Postal Codes table from Wikipedia + given locations from week 3 
Firstly, I made use of <a href="https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M">Toronto Postal Codes Table</a> to scrap the table to create a data-frame. For this, I’ve used requests and Beautifulsoup4 library to create a data-frame containing the Postal Codes, Borough and Neighborhood. Given the data in week 3, I have including the latitude and longitude into the data frame. We start as below —
(insert pic 1)
#### b. Filtering out the neighborhoods
Next, I decided as a tourist, I would be more interested in areas that the borough contains the word Toronto, thus, i filter those areas out. So the areas are namely, Downtown Toronto, East Toronto, West Toronto and Centeral Toronto. 
(insert picture 2)
With the data that is left, I went ahead to use Foursquare API to retrieve information about the popular spots around these 4 borough of Toronto. The popular spots returned depends on the highest foot traffic and thus it depends on the time when the call is made. So we may get different popular venues depending upon different time of the day. The call returns a JSON file and we need to turn that into a data-frame. Here with the limit of 100 and a radius of 500, I have gotten the data of 238 unique category of venues . Below is the data-frame obtained from the JSON file that was returned by Foursquare —
(insert picture 3)

#### c. Finding out Popular sites near the neighborhood
Using the data given by Foursquare API, I have used one hot encoding to find out which venues are the most common areas that the residents likes and head there often. The results are as follows--
(Insert pic 4)

#### d. Popular site - Cafe
As I have decided that I'll be around the studio district, I went ahead to look at the most common venue, Cafe. With this I went on to Foursquare API again and search for the nearby Cafes in the area!
(Insert pic 6)
*Purple Pengiun Cafe* - well the name of the cafe definitely caught my eye! Let's check the review on it!
(insert picture 8)
Good Review!! Let's go! But wait a minute! Let's first check out the neighborhood, if it is safe and worth going or if we should be more prepared before going. 

#### e. Toronto Police Service Public Data Portal
This dataset can be download from the <a href="http://data.torontopolice.on.ca/">Toronto Police Service Public Data Portal</a> and reflects reported incidents of crime (with the exception of murders where data exists for each victim) that occurred in the City of Toronto from 2014-2019, minus the most recent seven days. A full desription of the data is available on the site.

In order to protect the privacy of crime victims, addresses are shown at the neighborhood, Hood_ID. To learn more about the Hood_ID you can click <a href="https://www.toronto.ca/city-government/data-research-maps/neighbourhoods-communities/neighbourhood-profiles/">here</a>


