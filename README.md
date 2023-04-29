# Group-Project-2

## MIST4610 Group 21482_9



## Authors

- Ethan Watts      [@wattsxx](https://www.github.com/wattsxx)
- Michael Wagner   [@Mikecwagner21](https://www.github.com/Mikecwagner21)
- Angela Canales   [@Angeladc](https://www.github.com/Angeladc)
- Joe Murphy       [@josephgmurphy](https://www.github.com/josephgmurphy)
- Nakul Sajan      [@nakulsajan](https://www.github.com/nakulsajan)


## Questions and Significance

Question 1: Does the amount budgeted for a movie affect the success at the box office, and is there a trend between the ROI and their movie rating?

 This question is important because it evaluates whether or not movies with higher budgets are more successful within the box office (revenue). We often expect that movies with high budgeting, such as sci-fi and superhero movies, take the cake in terms of box office revenues compared to movies with lower budgets. This question will evaluate whether this assumption is true or not using an extensive data set representing the relationship between a variety of movie budgets and their box office revenue. In terms of the film industry, this question may be used to determine whether or not a movie will be successful upon release in theaters, and may be helpful in predicting how much of a ROI it will generate. Not only will this question address this, but it will also address the relationship between the movie’s budget and its efficiency rating (ROI x movie rating) amongst the general public. We usually expect a movie with a higher budget to have overall higher rates of success, and our efficiency rating calculation essentially measures the rate of overall success. However, given that the data set represents movies from the years 1921 to 2022, a higher budget with a high efficiency rate may not always be the case. Our discoveries based on this question could be helpful in predicting whether or not a movie will be successful in both ratings and ROI based on its budget. Overall, this question could be helpful in predicting the success of newly-released and future movies amongst movie enjoyers, the film industry, and anyone who is curious in general. 

Question 2: Since the IMDB was created in 1990, is there recency bias in Imdb rated drama movies?

This question addresses whether or not movies within recent years tend to be rated higher than those made several decades ago within the popular film online database, IMDB. Movie enjoyers tend to look at IMDB and their ratings when determining which movies are worth watching and which ones aren’t. However, IMDB was created in the year 1990, so we wonder if there is a recency bias within the 250 highest rated movies within the drama genre on the IMDB from the year it was established to the present. Our question and analysis will evaluate whether or not there is a recency bias between drama movies created from 1990 - 2022 based on a trend, which could reveal that the IMDB is not as credible as it should be in terms of rating the top 250 movies of all time. This could be impactful in terms of drama movie enjoyers or the general public not relying on the IMDB like they used to for this kind of data due to their potential biases. 

![EffeciencyRating](https://github.com/wattsxx/GroupProject2-TableauGraphs/blob/main/Screenshot%202023-04-28%20160049.png)

IMDb is the largest database of movies and television shows. This dataset consists of the top 250 movies IMDb rates since 1921 through 2022. This list contains pertinent information to these 250 movies including, rank, year, rating, budget and box office. This list was last updated in 2022 and doesn’t contain any movies in 2023. The columns are rank, which lists the rank the movie is out of 250, rated by IMDb. Name, which lists the movie name. Year, which displays the year the movie was released. Rating shows the movie critics’ rating of the movie out of 10. Genre shows the genre of the movie out of broad categories such as horror, action, or thriller. Certificate displays whether the movie was G, PG, PG-13, or R. Run_time shows the timestamp of the length of the movie. Tagline displays a famous line from each movie. Budget shows the amount of money they spent to make the movie. Box_office shows the amount of money the movie made from theaters. Casts lists all the actors that performed in the movie. Directors, lists the director(s) who directed the movie. Writers lists the writers who made the movie. We found this data set through Kaggle.
![RecencyBias](https://github.com/wattsxx/GroupProject2-TableauGraphs/blob/main/Screenshot%202023-04-28%20160652.png)

![RatingTotalsOverYears](https://github.com/wattsxx/GroupProject2-TableauGraphs/blob/main/Screenshot%202023-04-28%20162525.png)

## Description

This final graph is to confirm our findings found in our recency bias graph. We found that there was a slight trend upwards for the newer years. In this graph we took the sum of the ratings, and displayed it across years. This works to show that the newer years have a higher overall sum of ratings. Had this been a dataset of a random set of movies this would not work, however this dataset already shows the top 250 movies, meaning that by providing the sum of ratings shows that years may have had multiple movies all within the top 250. We had a definite peak around the 90s, which was anticipated. We hypothesized that this could be a trend once we found that IMDB was started in the 90s, and this graph confirms our hypothesis. 

![Workbook](https://github.com/wattsxx/Tableau-GroupProject2-Workbook/blob/main/MIST%20Tableau%20project.twb)

## Manipulations and Calculations
For our first question, our goal was to visualize what movies performed the best with the amount of money they had available to them. The determinants for this performance we decided would be the money made at box office and the final rating given to the movie by IMDb. Of course, these variables alone don’t paint a picture of how efficient the movie was because it doesn’t take into account budgeted money for the films. Thus, we had to create a new field called Efficiency Rating. This field involved taking two already existing fields in the data set, ‘budget’ and ‘box_office’, and turning them into a ratio. After dividing ‘box_office’ by the ‘budget’ of each movie, we then multiplied this ratio by the final IMDb rating to rank the efficiency of the movie. One problem we ran into when attempting to create this calculated field was the string value data types. In the original data set, the box office and budget fields were of the string data type. As a result, we changed these fields into number data types so the calculation would operate correctly.


With regards to our second question, we wanted to examine the relationship between time(year the movie was released) and the rating IMDb gave the movie. Thus, we took these two existing fields located in the data set and created a scatterplot to visualize ratings of the movies over time. We then went one step further by using a regression line. This regression line that we incorporated into our scatterplot allowed a more in depth analysis of the correlation between the two variables. After using this regression line to determine correlation, we were then better able to see if there was recency bias in the data set. In other words, did IMDb tend to give recent movies higher ratings as opposed to older ones?
