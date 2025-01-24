# ML_Movie_Recommender
Movie Recommender System
A content-based movie recommender using TMDB's top 10K movies dataset. Combines movie descriptions and user watch history to suggest similar films.

# Get recommendations

watchHistory = ['Your Name.', 'Spirited Away']

recommend('Iron Man', watchHistory)


Uses movie descriptions and genres for recommendations
Weights: 40% content similarity, 60% genre preference

Returns top 15 similar movies

Data Required

CSV file with columns: id, title, overview, genre

Note: Built for Google Colab. Data path: '/content/drive/MyDrive/Colab Notebooks/top10K-TMDB-movies.csv'
