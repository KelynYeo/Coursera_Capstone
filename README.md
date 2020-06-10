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
#### a. Scraping Toronto Postal Codes table from Wikipedia
Firstly, I made use of <a href="https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M">Toronto Postal Codes Table</a> to scrap the table to create a data-frame. For this, I’ve used requests and Beautifulsoup4 library to create a data-frame containing the Postal Codes, Borough and Neighborhood. We start as below —
<img src="1.png" alt="1">
