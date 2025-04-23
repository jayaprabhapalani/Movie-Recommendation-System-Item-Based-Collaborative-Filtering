# 🎬 Movie Recommendation System using MovieLens Dataset

This project explores multiple types of movie recommendation systems using the MovieLens 100K dataset, focusing on:

1.Item-Based Collaborative Filtering (IBCF)

2.User-Based Collaborative Filtering (UBCF)

3.Matrix Factorization (SVD)

4.Content-Based Filtering (CBF)
 
# Approach 1: Item-Based Collaborative Filtering (IBCF)

Recommends movies that are similar to a given movie based on how users have rated them.

Steps:

Load and merge ratings and movie metadata.

Create a user-item pivot table.

Compute cosine similarity between item vectors (movies).

Given a movie, recommend top N similar movies based on similarity.



# Approach 2: User-Based Collaborative Filtering (UBCF)

Recommends movies based on what similar users have liked.

Steps:

Build the user-item rating matrix.

Compute cosine similarity between users.

Find Top-K similar users for a given user.

Predict unseen movie ratings using weighted average.

Recommend top N movies with highest predicted scores.


# Approach 3: SVD-Based Collaborative Filtering

Uses Truncated SVD (matrix factorization) to uncover latent features of users and movies, helping recommend even in sparse scenarios.

Why SVD?

SVD is better than UBCF and IBCF for capturing hidden relationships and performing well on sparse datasets.

Steps:

Build user-item matrix.

Apply Truncated SVD to reduce dimensions.

Compute cosine similarity in the latent space.

Recommend top N similar movies to a given movie.


# Approach 4: Content-Based Filtering (CBF)

Recommends movies based on features of the content (e.g., genres, movie overview), independent of other users' ratings.

Steps:

Extract movie features (genres, overview, etc.).

Combine them into a text field (genres + overview).

Convert this text into TF-IDF vectors.

Compute cosine similarity between movie vectors.

Recommend top N movies similar to the input movie based on content.

Why Content-Based?
Works well for new users or items, since it relies on content, not past ratings.
