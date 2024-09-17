# Movie Recommender System

This project implements a movie recommendation system that suggests movies similar to a given movie title. The system uses movie metadata, vectorizes the text data, calculates cosine similarity between movie features, and recommends the top 5 most similar movies. The dataset was enhanced using the TMDB API to fetch additional movie data.

## Project Overview


This project allows users to input a movie title and receive recommendations for other similar movies. The similarity between movies is calculated based on cosine similarity of vectorized text features.

## Features

#### Text Vectorization: 
 The movie metadata (such as the title and other relevant features) is vectorized using CountVectorizer from scikit-learn.

#### Cosine Similarity:
Cosine similarity is used to compute the similarity between the movie vectors to find the most similar movies.

#### Movie Recommendations:
The recommender suggests 5 movies that are most similar to the movie input by the user.

#### TMDB API Integration: 
The TMDB (The Movie Database) API was used to fetch movie details such as metadata, genres, and descriptions, enhancing the dataset used for recommendations.


## Data Collection

The movie dataset was fetched and augmented using the TMDB API. You can get an API key from TMDB here.

Steps to fetch data:

1) Obtain your TMDB API key.
2) Use the API to fetch movie metadata such as genres, overviews, etc.
3) Store the fetched data for future recommendations.

## Model Persistence

To avoid recalculating the cosine similarity each time, the movie data and similarity matrix are saved as .pkl files:


## Deployment

Deployed the final model using Streamlit, creating an interactive web application where users can input an movie and 5 similar recommendation will be shown.

## Future Work

1. Add more sophisticated natural language processing (NLP) techniques for feature extraction.
2. Implement a hybrid recommendation system using collaborative filtering and content-based filtering.
3. Improve UI by building a web app using Flask or Streamlit.
4. Fetch more detailed movie information using the TMDB API (such as cast and crew).
