# Analysis of the Movie Industry

![Header](https://github.com/dicchyantgurung/Exploratory-data-analysis-of-the-movie-industry/blob/main/Images/Movie%20header.jpeg)

## Business Case:

All the big companies are now getting in on creating their own video content. However, success of these new ventures largely depend on creating the right content.


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

### 1. Pre-Processing

* Create a master dataset by merging all provided datasets using a unique key.
* Drop any irrelevant columns.
* Remove or fill missing values.

### 2. Data Analysis

* Perform EDA with proper visualization to answer all objectives.

### 3. Conclusion

------------------------------------------

## Exploratory Data Analysis

The master dataset is created by merging all six IMDB datasets. Missings values, irrelevant columns, and duplicates have been deleted accordingly to fit the purpose of the project.


### EDA 1. Genre Analysis

For the first part of the project, we will need to get a total count of 'Average Rating' received for each genre. The one problem with this dataset is that some movies are tagged across multiple genres. Nevertheless, because the movie constitutes all genres that it was tagged to,
it is safe to assume that each genre is a separate instance and that the average ratings received will be the same across each of the genres for the same movie.

The column with multiple genres are split into individual columns. This is then combined back into a single column creating different rows for each genre within a movie. 

The resultant dataset now can be grouped together by genres using mean to give us a final count of average ratings for each genre.

A horizontal bar graph can be used to give us a visual representation of ratings received for each genre.

![AVERAGE RATING GRAPH](https://github.com/dicchyantgurung/Exploratory-data-analysis-of-the-movie-industry/blob/main/Images/Average_Rating.png)

It seems that on average, 'Documentary' is the highest rated of all times followed by 'Game-Show'. 'Horror' and 'Adult' seems to be the least ranked categories.

However, it is also important to note that not all generes received the same amount of votes. The graph above might not be the true repesentation of ratings received for each genre. We will use the number of votes received
to create a weighted average raing. This will give us a true representation of ratings received for each genre.

![WEIGHTED AVERAGE RATING GRAPH](https://github.com/dicchyantgurung/Exploratory-data-analysis-of-the-movie-industry/blob/main/Images/Weighted_Average_Rating_Votes.png)
  
It is clear that 'Drama' is the winner followed by 'Action', 'Adventure' and 'Comedy'. 'Documentary', 'Game-Show', and 'News' seem to have been incorrectly classified before as there were only few good votes for them. 
 

### EDA 2 . Genre Outreach

For this part of our project, we are looking to analyze the popularity of each genre. This will give us a good indication on what movies people are most likely to watch when it comes out. Ratings are a good indicator of movie interest, but it is also good to have an idea of what genres are people talking about the most.

With the data spanning across 10 years, it is safe to assume that the number of votes received can be equivalant to people being interested in watching the movie and participating in the voting process. Hence, the likelihood of the movie being watched can be estimated by the total number of votes received. 

A simple sorting of 'Number of votes' column gives us a good idea on what genres are crowd favourites. A tree map is used here to represent this distribution.

![TREE MAP](https://github.com/dicchyantgurung/Exploratory-data-analysis-of-the-movie-industry/blob/main/Images/Tree_Map.png)

Here, we can see that 'Drama' has the largest box, which means that it captures the most audience. 'Action', 'Adventure', and 'Comedy' follows similarly.


### EDA 3. Time-Series Analysis

It is also good to know how many types of movies are been produced each year. This will give us an idea about the changing interest or trend that the population is following in terms of genre preference.

For this part of the project, we will need to calculate the total number of movies produced per year for each genre.

A line graph can be used to plot number of movies produced each year for all genres.

![ALL GENRE LINE GRAPH](https://github.com/dicchyantgurung/Exploratory-data-analysis-of-the-movie-industry/blob/main/Images/Time_Series_All_2.png)

There seems to be an overall decreasing trend in movie production. The most produced genre is 'Drama', 'Documentary', 'Comedy', and 'Thriller'. There is a steady production of all these genres over the years except for 'Documentary', which shows a decreasing interest from the public.

We can plot more graphs for other lists explored in the EDA to confirm the trend. 

![TOP 5 LINE GRAPH](https://github.com/dicchyantgurung/Exploratory-data-analysis-of-the-movie-industry/blob/main/Images/Time_Series_Top_5.png)
![TOP 5-10 LINE GRAPH](https://github.com/dicchyantgurung/Exploratory-data-analysis-of-the-movie-industry/blob/main/Images/Time_Series_Top_5-10.png)


## Conclusion

According to the analysis, we can make the following conclusions:

- Drama, Action and Adventure are currently doing the best in the box office.
- These three genres are all highly rated with a combined average-rating of 6.1, which falls third in the individual scale.
- They also capture almost 50% of the entire movie community.

We were also able to see that there has been a decreasing trend in the overall production of all movies. This can be correlated to the recent boom of social media and rise of short-form content consumption. However, we do not have enough data to prove this yet. The decrease in movie production can also be seen as an opportunity with less competetion as movies are still a big part of our daily lives. 

## Recommendation

*1. Create content in either Drama, Action, and/or Adventure.*

All these three genres are high in demand and will provide the best chance of success if we embark in creating movies with similar content. They also represent almost 50% of the entire movie community, which will ensure high sales and quick promotion of the movie studio.

*2. Create movies mixing different genres.*

Using Drama, Action, and Adventure as base, we can incorporate new genres which will appeal to a wider audiences and draw new customers to the brand.

*3. Release movies in different languages.*

Different languages will capture different regions, allowing you to re-introduce the same product in different markets and increase the overall profitability.

 






