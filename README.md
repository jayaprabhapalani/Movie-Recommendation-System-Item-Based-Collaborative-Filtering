# 🎬 Movie Recommendation System using MovieLens Dataset

This project explores two fundamental types of recommendation systems built using the [MovieLens 100K dataset]:

1.  **Item-Based Collaborative Filtering** using **Cosine Similarity**
2.  **User-Based Collaborative Filtering** using **Top-K Nearest Neighbors**

---

##  Approach 1: Item-Based Collaborative Filtering

This method finds **similar movies** based on user ratings and recommends movies **similar to a target movie**.

###  Steps:

1. Load and merge `ratings.csv` and `movies.csv`.
2. Create a pivot table (user-movie matrix).
3. Calculate **Cosine Similarity** between movie vectors.
4. Choose a **target movie** (e.g., *Star Wars*).
5. Find similar movies with a sufficient number of ratings.
6. Recommend **top N similar movies**.

###  Example Output:
Top 10 movies similar to **Star Wars (1977)** based on cosine similarity and rating overlap.

---

##  Approach 2: User-Based Collaborative Filtering

This method finds **users similar to the target user** and recommends movies that similar users have liked, but the current user hasn't watched.

### Steps:

1. Build the **user-item matrix** (pivot table of ratings).
2. Calculate **Cosine Similarity between users**.
3. For a given `user_id`, find **Top-K most similar users**.
4. Use **weighted average of their ratings** to predict scores for unseen movies.
5. Recommend top N movies with the highest predicted scores.

###  Example Output:
Top 10 movies **predicted for user 1** using preferences of the top 5 similar users.





