# Movie-Recommendation-System-Item-Based-Collaborative-Filtering
This project builds a simple movie recommender system using Item-Based Collaborative Filtering with the MovieLens 100K dataset.
Steps
Load and Merge Data
Merged movie ratings and movie titles using movie_id as the key.

User-Item Matrix
Created using pandas pivot_table.

Rows → users

Columns → movie titles

Values → ratings (NaN if not rated)

Item-Item Similarity
Used pandas.corrwith() to compute similarity between a target movie and all others.

Filtering
Only considered movies with more than 50 ratings to ensure reliable similarity.

Recommendation
Recommended top N movies similar to a selected target (e.g., Star Wars (1977)).

