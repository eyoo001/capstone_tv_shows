# Table of Contents

Notebook breakdowns

| Number | Name |
| --- | --- |
| 00 | [ONLY THIS ONE](./Capstone/Working in Currently/List_of_Shows.ipynb) |
| 01 | [Wiki](./Capstone/Data/Grabbing Wiki Links & Names.ipynb) |
| 02 | [Wiki2](./Capstone/Data/Wiki API.ipynb) |
| 03 | [TVDB](./Capstone/Data/TVDB API.ipynb) |
| 04 | [OMDB & TMDB](./Capstone/Data/OMDB_TMDB API.ipynb) |
| 05 | [OMDB](./Capstone/Data/OMDB_API.ipynb) |
| 06 | [Wiki_Alt](./Capstone/Data/Wiki_Alt.ipynb) |
| 07 | [TMDB_API](./Capstone/Data/TMDB_API.ipynb) |


## 01
#### Webscraping + Wiki API
- Function to grab links for shows per network

## 02
#### Webscraping + Wiki API
- List of network urls (122)
- Cleaned list of network names
- Dictionary of shows by network
- Cleaned list of shows by network

#### Out of scope
- Gathering table data from shows with Wiki API
- Viewership info
- Writers
- Directors
- Episode Synopsis


## 03
#### TVDB API
- Status
- FirstAired date
- Network
- Runtime
- Genre
- Overview 
- AirDaysofWeek
- AirsTime
- imdbID
- AiredEpisodeNumber
- AiredSeason
- Directors
- GuestStars
- Overview
- Writers

## 04
#### OMDB API Wrapper
- Awards?
- Director
- Genre
- Episode
- Season
- Plot
- Ratings
- Runtime
- Writer
- imdbID
- imdbRating

#### TMDB API Wrapper
- Total number of episodes per season
- Total number of seasons
- Runtime
- Airdate
- Month
- Day of week
- Writer
- Producer
- Director
- Network
- Overview summary
- Genre
- Status

## 05
#### OMDB API Wrapper Attempt 2


## 06
####  Wiki Alt


## 07
#### TMDB API



# Data Dictionary
### clean list
- List of cleaned tv shows using regex
- ~63k
### network_dict.json
- Dictionary of Networks to TV shows pulled from Wikipedia
- 122 Keys
- 93k Values
### new_show_list
- List of cleaned tv shows from the Wiki Categories page (2010+ shows)
- 2.5k 
### show_list
- Show names with the cites/blanks/etc names removed
- 63k
### test_list
- List of OMDB series information
- 13k
- Can likely delete - too many nulls
### omdb_list
- Dictionary
- 12k Keys
- Improved version of test_list
### Untitled Spreadsheet
- List of tv network URLs on wikipedia pulled via XPath



# The Question
Automation through machine learning is quickly permeating all industries, allowing for greater insight into practices with less labor involved. Depite the practical applications of these simple, yet effective algorithms, Hollywood appears to be slow to fully utilize the extent of their data. 

Using existing data available publically on the Internet, is it possible to reduce the uncertainty in guessing the public sentiment of new and current television shows? If networks and producers can accurately predict how the viewing public will receive a show before even making the pilot, there would be no more need for the traditional (and archaic) bean counters and scriveners that have previously determined the livelihoods of current and future shows. And machine learning models will never simply reply "I prefer not."


# The Statement
With a combination of NLP and regression machine learning models,


# The Approach
I intend to use multiple models to try and maximize the efficacy of the final model for production. The final target value that I will be attempting to predict is the IMDB rating. 

- The writers will need to be assigned weights based on how often they have written for shows and how those shows were received. This can be handled as a
- I would like to determine if there are key themes, topics or motifs that are more common in successful (critically) shows than not. I may be able to utilize TF-IDFing or LDA in order to extract any key terms from the plot summaries and loglines from the show(s).
- Once all the other information is compiled into a single dataset, I will use regression functions to try and best predict how new shows will be received
- Alternatively, this could also be approached as a classification problem by categorizing the ratings - this would also be beneficial in that the NLP could be integrated with less munging. 
- I believe it would also be interesting to attempt unsupervised learning with Neural Networks.
- Clustering/PCA for feature selection


# The Dataset



How the number of votes on IMDB affect the rating - more ratings will have a slightly lower rating overall
- Shows that have low popularity with imba score vs shows with high number of ratings having a lower or higher rating
