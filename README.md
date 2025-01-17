# ML_Movie_Recommender
Movie Recommender System
A content-based movie recommender using TMDB's top 10K movies dataset. Combines movie descriptions and user watch history to suggest similar films.

Setup

pythonCopyimport pandas as pd

from sklearn.feature_extraction.text import CountVectorizer

from sklearn.metrics.pairwise import cosine_similarity

Usage

pythonCopy# Add your watch history

watchHistory = ['Your Name.', 'Spirited Away']


# Get recommendations
recommend('Iron Man', watchHistory)

How it Works

Uses movie descriptions and genres for recommendations
Weights: 40% content similarity, 60% genre preference

Returns top 15 similar movies

Data Required

CSV file with columns: id, title, overview, genre

Note: Built for Google Colab. Data path: '/content/drive/MyDrive/Colab Notebooks/top10K-TMDB-movies.csv'
