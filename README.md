# Wrangle-and-Analyze-Data-WeRateDogs

## Introduction
**Udacity: Wrangle and Analyze data** <br>
The goal is to wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. <br>
The Twitter archive is great, but it only contains very basic tweet information. Additional gathering, then <br>
assessing and cleaning is required for worthy analyses and visualizations.


## Gathering Data
I gathered data from three sources:
- The WeRateDogs Twitter archive - A file provided by Udacity
- Images prediction files - A file downloaded programmatically from Udacity server
- Additional data from the Twitter API - gathering through Twitter API

## Assessing Data
I assessed the data both visually and programmatically and identified the following quality and tidiness issues for <br>
each table:
#### Quality Issues
#### `Archived` table

- Erroneous data type for timestamp and Tweet id
- Drop extraneous columns (Retweets and reply columns) and rows. We are only interested in the original tweets.
- Source links should be shortened
- Rating denominator has values greater than 10
- Rating numerator has large values like 960 and 1776
- Name column contains some wrong names like a, an, the, just, very, quite etc
- Remove rows without dog images
- Drop null values

#### `Twitter API` table
- Tweet id should be a string and not integer
- Missing data. The data has 33 rows less than the twitter archived

#### `Images` table
- Tweet id should be a string and not integer
- Missing data. The data has 281 rows less than the twitter archived

#### Tidiness Issues

- Dog stages in the archived table should be in one column and not four columns
- Multiple columns in the Images table for dog breeds and confidence predictions
- Twitter API and Images tables should be part of archived table

## Cleaning Data
I started by changing the data types for timestamp column in the archived table and the tweet_id columns in all the tables. <br>
Thereafter, I resolved all the tidiness issues to give my data the right structure. The result of cleaning the tidiness <br>
issues is the structured archived master data which has combined all the three datasets together.

Thereafter, I cleaned all the remaining quality issues by removing columns like retweets and replies not related to the <br>
original tweets. I manually updated the right numerator and denominator ratings and removed the 12 rows with the ratings <br> 
I could not find. And lastly, I replaced the wrong names like a, an, just, and so on with None. 

## Storing Data
The result of this wrangling is the cleaned master data with 1946 rows and 13 columns stored as a csv file named <br>
`twitter_archive_master.csv`. And this cleaned master data formed the basis for my analyses and visualizations.

Warm Regards
### Olamide Emida
