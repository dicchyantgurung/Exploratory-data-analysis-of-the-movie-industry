# Analysis of the Movie Industry

## Project:

* Perform data analysis and create a presentation that explores what types of films are currently doing best at the box office.

## Dataset:

* IMDB

IMDB is one of the most credible sources out there for movie-ratings and popularity. This should provide us with enough quality data to perform our EDA and arrive at a conclusion for our project. 

## Objective:

1. Identify what genres have the the highest ratings in IMDB 
* Genre Analysis

2. Analyze what genre is most likely to be watched or is preferred by most 
* Genre Outreach

3. Analyze the trend in movie production per genre over the years
* Time-Series Analysis

## Assumption:

* The data received from IMDB is the most accurate representation of people's choice and preference in movies.
* All ratings received are unbiased when compared across different genres in terms of production quality, direction, actor's performance and region of debut.

## Process Overview:

1. Pre-Processing

* Create a master dataset by merging all provided datasets using a unique key.
* Drop any irrelevant columns.
* Remove or fill missing values.

2. Data Analysis

* Perform EDA with proper visualization to answer all objectives.

3. Conclusion

## EDA:

The master dataset is created by merging all six IMDB datasets. Missings values, irrelevant columns, and duplicates have been deleted accordingly to fit the purpose of the project.

1. Genre Analysis

For the first part of the project, we will need to get a total count of 'Average Rating' received for each genre. The one problem in this dataset is that some movies are tagged across multiple genres. Because the movie constitutes all genres that it was tagged,
it is safe to assume that each genre is a separate instance and that the average ratings received will be the same across each of the genres for the same movie.

The column with multiple genres are split into individual columns. This then is combined back into a single column creating different rows for each genre within a movie. 

The resultant dataset now can be grouped together by genres using mean to give us a final count of average ratings for each genre.

A horizontal bar graph can be used to give us a visual representation of ratings received for each genre.

![AVERAGE RATING GRAPH](https://github.com/dicchyant84/Module_1_Final_Project/blob/main/Graphs/Average_Rating.png)

It seems that on average, 'Documentary' is the highest rated of all times followed by 'Game-Show.' 'Horror' and 'Adult' seems to be the least ranked categories.

However, it is also important to note that not all generes received the same amount of votes. The graph above might not be the true repesentation of ratings received for each genre. We will use the number of votes received
to create a weighted average raing. This will give us a true representation of ratings received for each genre.

![WEIGHTED AVERAGE RATING GRAPH](https://github.com/dicchyant84/Module_1_Final_Project/blob/main/Graphs/Weighted_Average_Rating.png)
  
It is clear in the above graph that 'Drama' is the winner followed by 'Action', 'Adventure' and 'Comedy'. 'Documentary', 'Game-Show', and 'News' seem to have been incorrectly classified before as there were only few good votes for them. 
 
2 . Genre Outreach

For this part of our project, we are looking to analyze the popularity of each genre. This will give us a good indication on what movies people are most likely to watch when it comes out. Ratings come second, so it is good to 
have an idea of what genres interest the most.

With the data spanning across 10 years, it is safe to assume that the number of votes received can be equivalant to people being interested in watching the movie and participating in the ratings count. Hence, the likelihood of the movie being watched
due to it's genre.

A simple sorting of the 'Number of votes' can give us a good idea on what genres are crowd favourites. A pie chart can be used to represent this distribution. The pie being the total audience in the market and each slice representing the market capitalization(interest) of each genre within the population.

![PIE CHART](https://github.com/dicchyant84/Module_1_Final_Project/blob/main/Graphs/pie_chart.png)

Here, we can see that 'Drama' has the most reach out of all, which means that it captures the most audience. 'Action', 'Adventure', and 'Comedy' follows similarly.

3. Time-Series Analysis

It is also good to know how many types of movies are been produced each year. This will give us an idea about the changing interest or trend that the population is following in terms of genre preference.

For this part of the project, we will need to calculate the total number of movies produced per year for each genre.

A line graph can be used to plot number of movies produced each year for all genres.

![ALL GENRE LINE GRAPH](https://github.com/dicchyant84/Module_1_Final_Project/blob/main/Graphs/All_Rated.png)

From this graph we can see that there is an overall decreasing trend in movie production. However, the decrease is not substantial by any means.
The most produced genre is 'Drama', 'Documentary', 'Comedy', and 'Thriller'. There is a steady production of all these genres over the years except for 'Documentary', which shows a decreasing interest from the public.

We can plot move graphs for other lists explored in the EDA to confirm the trend. 

![TOP 5 RATING LINE GRAPH](https://github.com/dicchyant84/Module_1_Final_Project/blob/main/Graphs/Top_5_Rated.png)
![TOP 5 MOST PRODUCED LINE GRAPH](https://github.com/dicchyant84/Module_1_Final_Project/blob/main/Graphs/Most_5_Produced.png)
![LEAST 5 PRODUCED LINE GRAPH](https://github.com/dicchyant84/Module_1_Final_Project/blob/main/Graphs/Least_5_Produced.png)

## Conclusion

According to the data we have available for this EDA, we can confirm that Drama, Action and Adventure seems to be doing the best in the box office today. They are all highly rated and also represent a big population within the moviegoers.
The combined average rating comes out to 6.1, which falls third in the individual scale. While also capturing 44.5% of total interest in the movie community.  






 
 






