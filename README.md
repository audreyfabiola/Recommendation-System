# User-Based Recommender System for Cellphones

This project implements a user-based recommendation system for suggesting cellphones to users based on their preferences and ratings. The recommendation system uses the Pearson correlation coefficient to find similar users and recommends cellphones that these users have liked.



### Implementation Details

##### 1. Input Data

The system relies on two CSV files:The recommendation system uses two CSV files:

- `cellphones_data.csv`: This file contains detailed information about various cellphone models, such as the cellphone ID and model name.
- `cellphones_ratings.csv`: This file contains user ratings for different cellphones, associating a user ID, cellphone ID, and a rating.

##### 2. User Input

Users can input their preferences by modifying the `userInput` dictionary in the script. This dictionary includes cellphone models and corresponding ratings.

##### 3. Similarity Calculation

The system calculates user similarity using the Pearson correlation coefficient. It identifies the top users with the most similar preferences to the input user, based on the ratings they have given to common cellphones.

##### 4. Weighted Ratings

The script then calculates weighted ratings for each cellphone, taking into account both user similarity and user ratings. The more similar a user is to the input user and the higher their ratings, the more impact their ratings have on the recommendations.

##### 5. Recommendation Generation

The system generates cellphone recommendations by calculating the weighted average recommendation score for each cellphone. The recommendations are sorted based on the score in descending order, and only highly recommended cellphones (with a score greater than 4.9) are displayed.