# ML_Movie_Recommender
Movie Recommender System
A machine learning-based movie recommendation system that suggests movies based on content similarity and user watch history. The system uses the TMDB (The Movie Database) top 10,000 rated movies dataset and implements a hybrid recommendation approach combining content-based filtering with user preferences.
Features

Content-based movie recommendations using movie descriptions
User preference consideration through watch history
Hybrid recommendation system combining content similarity with genre preferences
Weighted similarity scoring (40% content, 60% genre preference)
Returns top 15 movie recommendations

Technical Implementation
Dependencies

pandas
scikit-learn (sklearn)

CountVectorizer
cosine_similarity



Data Processing

Uses TMDB top 10K movies dataset
Processes movie descriptions using natural language processing
Features extracted:

Movie ID
Title
Overview (converted to tags)
Genre



Algorithm

Text Processing:

Tokenizes movie descriptions using CountVectorizer
Removes English stop words
Creates feature vectors (max 10,000 features)


Similarity Calculation:

Computes cosine similarity between movie descriptions
Generates genre preference vector from watch history
Combines content and genre similarities with weighted scoring



Usage
pythonCopy# Initialize watch history with previously watched movies
watchHistory = ['Your Name.', 'Spirited Away', 'Everything Everywhere All at Once', 'Singin\' in the Rain']

# Get recommendations based on a recently watched movie
recommend('Iron Man', watchHistory)
Functions
recommend(watched, watchedHistory)
Parameters:

watched: String - Title of the most recently watched movie
watchedHistory: List - List of previously watched movie titles

Returns:

Prints titles of 15 recommended movies

getPreferredGenresVector(watchedHistory)
Parameters:

watchedHistory: List - List of previously watched movie titles

Returns:

numpy array - Vector representation of preferred genres

Data Requirements
The system expects a CSV file with the following columns:

id
title
overview
genre

Note
This implementation assumes the data file is located at '/content/drive/MyDrive/Colab Notebooks/top10K-TMDB-movies.csv' and is designed to run in Google Colab.
