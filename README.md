# Microsoft Movie Analysis

**Author**: Gaja Sanchayan

## Overview

Microsoft have decided to create a new movie studio and require more insight into which types of films are doing best at the box office. This project uses descriptive statistical analysis on data gathered from IMDb, TMDB  websites to gain insight into which combination of genres topped the league in these areas. Four seperate datasets were used for this analysis to gain insight into which  genres of movies topped the box office,how the budget affects the Box office performance and also corelation between the average  rating and box office.
The results showed the consistently performing  movie Genres are Adventure and Animation followed by Action and Family.Also the high budgeted movies are generally performing well at box office. Based on budget again Adventure and Animation are generally high budget movies with high performance. Action and Family genres are the best for middle budget movies with consistent performance.The corelation between the average  rating and box office shows the films with high box office performance are also critically acclaimed well.
 



## Business Problem

Microsoft want to produce movies that are going to be successful in order to make profits, they want to know which types of movies are the most successful at box office. To answer that question Genres, Total gross income (domestic + Foreign),Budget and  Average Rating was analysed to see the most financially successful genres, and the budget corelation to box offcie performance and to see how average rating compared with financial success.


***

## Data

The data analysed came from IMDb and TMDB website. IMDb (an acronym for Internet Movie Database) is a popular worldwide online database of infomation relating to all movies, television programs, video games and streaming content online. TMDB (an acronym for The Movie Database)is anothe rpopular movie information site. 
I used 2 files from IMDb to get the Genre and Average rating parameters and 1 file from TMDB to get the domestic gross income,Foreign gross income and production budget.


## Methods

After checking the information on each table to see column names and null values, I joined the two datasets, imdb.title.basics and imdb.title.ratings together using the 'tconst' column as it was a unique identifier creating a new dataframe called mergeddf23.
I then splitted the multiple values in the 'Genre" column to individual values in the mergeddf23 Dataframe.
I then renamed the 'primary title' column to 'title' in the new data frame and renamed the 'movie' title to 'title' in the tn.movie_budgets.csv.gz from TMDB.
I then joined both of these dataframes using the title as the unique identifier, creating a combined new dataset called mergeddf24.

Checking the information on the new dataframe mergeddf24,I then duplicated this to a dataframe called  df5 and cleaned up the null values by removing them and dropped "original title" as it was not required  to carry out this analysis and
Then I  tidied up the "Domestic Gross' and 'Foreign Gross' columns by removing $ sign and converted them to units of  millions for easier readability and calculation. I then then added a new parameter called "box office" to df4 by adding both "domestic gross" and "Foreign gross"

## Results

Top HITS Genres are Animation and Adventure based on the box office vs Genre graphs.
Though Averagely Sci-fi and Fantasy performs well , 50% of  it is performing low than the averag.Hence Action & Family is the third and fourth Genre in terms of Reliable and consistant Box office performance. 
There is positive relationship between Budget and Box Office based on Budget and Box office. and it also shows Adventure and Animation movies are generally high Budget movies and Action and Family are generally middle budget movies 
The films with high box office performance are critically acclaimed well based on the Average rating.


## Conclusions

This analysis leads to three recommendations regarding types of movies that are successful:-

Adventure and Animation movies are generally high budget movies having high performance at box office. 
Action and Family genres are the best for middle budget movies with consistent performance.
The films with high box office performance are also critically acclaimed well

Questions to consider:

Limitations-the same movie be classified into different genres by different audiences? Who classifies the genres for each movie? Can the classification of genres be improved to provide a more benchmark approach?
Future analysis could include the movie classification ie PG, MA etc to see which audience the most successful movies were made for.
***




## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                           <- The top-level README for reviewers of this project
├── Project1-Gajanani.ipynb   <- Narrative documentation of analysis in Jupyter notebook
├── Presentation.pdf         <- PDF version of project presentation
├── data                                <- Both sourced externally and generated from code
└── images                              <- Both sourced externally and generated from code
```
