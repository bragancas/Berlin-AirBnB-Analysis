# Berlin AirBnB Analysis

A short data analysis project of AirBnB listings in Berlin. In particular, what association can be drawn between the characteristics, price and location for high performing listings? Are there any discernible factors within reviews underpinning these listings? Aspects of the analysis include data wrangling, exploratory analysis of price, location, property, user reviews data and basic topic extraction using user reviews.

## Background on data

The data was created by Murray Cox and can be found on his website [*insideairbnb*](http://insideairbnb.com). There is no private information available through this dataset and it uses only public information which can be found on Airbnb’s website. The location information for the listings has been anonymised by Airbnb with a deviation of 150 metres from the original location. The data is available in csv format in multiple files providing information on prices, listings location, listing neighbourhood, property type, deposit amount, user reviews, user ratings, etc. 

## Approach

1. View the listings data to get a general sense of the available columns and its content. Filter out columns irrelevant to analysis.
2. Deduplicate the data and ensure each column's data types are appropriate for further usage.
3. Impute NaN with appropriate values based on what each column represents and carry out a high level sanity check of the resultant data values.

4. Segregate exploratory analysis into various levels. First, analyse data on the listed properties(property types of the listings, overall room types, room types for each property type), then the price data (price for different room types, median prices within Berlin's various neighbourhoods, amount of reviews for various price points) and finally geographic analysis(general location clusters of listings, room types at the various locations, prices versus location).
5. Establish a cutoff to categorise higher performing listings using ratings score as well as number of reviews they recieved as a filter for popularity.
6. Analyse these high performing listings based on similar criteria as in point 4 to understand what could drive their performance and popularity.
7. For the high performing listings determine the common underlying factors indicated within the corpus of reviews. Filter out the non english reviews and perform text processing(tokenize reviews, remove characters/punctuation, numbers, stop words, lemmatize words). Create a wordcloud visualisation to view those words used frequently by customers in their reviews. Perform topic extraction using the non-negative matrix factorization (NMF) algorithm to identify overarching themes within the reviews.  


## Notebook preview
<p align="center">
<img src="https://github.com/bragancas/Berlin-AirBnB-Analysis/blob/master/Price%20per%20room.png"/>
</p>

<p align="center">
<img height="400" width="600" align="center" src="https://github.com/bragancas/Berlin-AirBnB-Analysis/blob/master/Room%20types%20vs%20location.jpeg"/>
</p>

<p align="center">
<img height="400" width="600" align="center" src="https://github.com/bragancas/Berlin-AirBnB-Analysis/blob/master/HP%20location%20vs%20price%20.jpeg"/>
</p>

<p align="center">
<img height="423" width="563" align="center" src="https://github.com/bragancas/Berlin-AirBnB-Analysis/blob/master/Wordcloud%20reviews.png"/>
</p>