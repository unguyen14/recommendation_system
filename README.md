# Movie Recommendation System

## Project Overview
This project aims to build a robust recommendation system that offers various suggestions methods, based on the movies themselves as well as the audience's preferences, using the datasets from [MovieLens](https://grouplens.org/datasets/movielens/25m/) and [The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset) from Kaggle.

**Main methodologies**
- Text Processing with [TF-IDF](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html)
- Machine Learning models: [KNeighborsRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsRegressor.html)
- Statistical Methods: [Jaccard similarity](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.jaccard_score.html#:~:text=Jaccard%20similarity%20coefficient%20score.,set%20of%20labels%20in%20y_true%20.), [Cosine similarity](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.pairwise.cosine_similarity.html)

## Project Motivations:
Learning users' behaviors through their interactions with the products can be applied to promote relevant items strategically, thus leading to improvement in user satisfaction. Some of the state-of-art recommending systems have been widely utilized by big companies like Netflix, Amazon, etc. 

This project is a collaborative effort of Winnie Nguyen and Fabio Turazzi, aiming to build a robust movie suggestion engine that takes advantage of a variety of available features. We use methods based on movie popularity, content filtering, collaborative filtering, and hybrid alternatives to maximize the relevancy to the recommendation output. 

## Recommendation Algorithms:
- **Simple Recommendation System**: generally analyzing most popular and highest rated movies across genres.

- **Content-Based Recommendataion**: using contents as the basis to suggest similar movies.
    - *Genre similarity*: recommendations based on the similarities between movie genres.
    - *Description similarity*: based on text similarities in movie descriptions.
    
- **Collaborative Filtering**: using ratings as the basis to suggest similar movies.
    - *Item-based filtering*: provides recommendations given a movie title by analyzing other items similarly rated by users.
    - *User-based filtering*: focuses on a target user to provide suggestions, by analyzing favorite movies by other similar users. Includes a model for rating prediction for a given user and movie.

## Datasets
We use 4 datasets obtained from the 2 sources mentioned above. 

- links.csv: containing movieId, imdbId, tmdbId (from MovieLens)
- movies.csv: containing movieId, title, genres (from MovieLens)
- ratings.csv: containing userId, movieId, rating, timestamp (from MovieLens)
- movies_metadata.csv: containing imdb_id, overview (from Kaggle with selected columns only)

### links.csv
Variable name | Description | Data Type
------------------ | ------------------------------------------------ | ---------
movieId | unique Id given to a movie on MovieLens | int
imdbId | ununique Id given to a movie on IMDB.com | int
tmdbId | ununique Id given to a movie on themoviedb.org | float

### movies.csv
Variable name | Description | Data Type
--------- | ------------------------------------------------ | ---------
movieId | unique Id given to a movie | int64
title | movie title | object
genres | movie's genres | object

### ratings.csv
Variable name | Description | Data Type
--------- | ------------------------------------------------ | ---------
userId | unique ID for each user | int
movieId | unique ID for each movie on MovieLens | int
rating | rating given to the movie by user | float
timestamp | timestamp of given rating | int

### movies_metadata.csv 
Variable name | Description | Data Type
--------- | ------------------------------------------------ | ---------
imdbId | ununique Id given to a movie on IMDB.com | object
overview | movie's overview | object

## Project Directory
```
| -  recommendation_system        
|   -- data                                         Includes all datasets used for the project
|     --- links.csv                                 
|     --- movies.csv
|     --- ratings.csv                               Not uploaded due to file size constraints
|     --- movies_metadata.csv                       Not uploaded due to file size constraints
|     --- additional_datasets.md                    Describes the path for two datasets that couldn't be uploaded to GitHub 
|   -- LICENSE                                      MIT License
|   -- Movie_recommendation_sys.ipynb               Google Colab Notebook with source code
|   -- README.md                                    Project Overview
```

## Potential Considerations
In this project, we were able to provide different perspectives to movie recommendation that can be used in a professional setting to generate a robust engine. Even though we were successfull in identifying item similarity, more methods can be explored to improve recommendations even further. 


