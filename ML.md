# ✉️ Phase 3 - Report

This phase we covered the feature engineering and modeling part of the project. I trained two different machine learning tasks using the cleaned IMDb + TMDB review datasets.

The two methods I used were:
1. Classification: Predict whether a movie is "scary" (1) or "not scary" (0)
2. Regression: Predict a movie's IMDb rating

## 1. Data Used & Modeling Table

I used the cleaned datasets from Phase 2:
- data_clean/movies_clean.csv → 836 movies
- data_clean/reviews_tmdb_clean.csv → 2099 reviews
which helped me create a movie-level dataset for modeling:
- data_clean/ml_table.csv

Modeling table contains 1 row per movie and in each row I have combined:
- metadata features (such as year, runtime, genre, votes/log_votes, etc.)
- review summary features (such as review_count, avg_review_rating, avg_review_length, etc.)
- fear-related features from review text (fear keyword ratios / density)

I created this table because the reviews are many-to-one, but ML models (from what ı understood) need fixed features per movie. So I aggregated review information per movie. 

## 2. What I added (feature engineering):

From review texts and ratings, I produced extra numeric features suh as: 
- review_count: how many reviews a movie has
- avg_review_rating = average TMDB rating
- avg_review_len = average review length
- fear_review_ratio = fraction of reviews that contain fear-related keywords
- other fear-related counts/density features 

In preprocessing part these features were:
- scaled using StandardScale,
- genre was converted using OneHotEncoder
- models were trained as pipelines (preprocess + model)

## 3. Method 1: Classification

### 3.1 Target:

For this part I created a binary label called scary using the feature fear_review_ratio.
- If a movie's fear above the median, Model label's it as scary = 1
- Otherwise scary = 0 (not scary)

This helps the models learn: can we predict whether a movie belongs to the higher level fear group?

### 3.2 Models tested:
I tried the method on some models before I choosed the final one which gives the best scores. Some models I used were:
- DummyClassifier (baseline)
- Logistic Regression
- Random Forest Classifier

And from these, the Final Model (Best Model) was: Random Forest Classifier

### 3.3 Results:

When I studied the results:

First I looked at Accuracy, because Accuracy is the simplest metric and shows how often the model predicts the correct class overall. However, since “scary” prediction can be harder than “not scary,” I also looked at the F1-score, which balances how many scary movies the model correctly finds and how many false alarms it gives. To understand what kind of mistakes the model makes, I used the confusion matrix (true/false positives and negatives). This helped me see whether the model tends to miss scary movies or incorrectly label non-scary movies as scary. For a more detailed view, I saved the predictions in predictions_classification.csv, which includes each movie’s true label and predicted label.

## 4. Method 2: Regression

### 4.1 Target:

The target in this part was imdb_rating, since this method trained models to predict imdb ratings of movies.

### 4.2 Models Tested: 

Models tested were: 
- DummyRegressor (mean baseline)
- Ridge Regression
- Random Forest Regressor

Final best model was: Random Forest Regressor 

### 4.3 Results: 

When I studied the results in the secon part: 

I focused on MAE/RMSE/R² because they explained the regression performance in different ways. For example, MAE showed the typical error size in IMDb rating points, which was easy to interpret. Since RMSE penalizes larger mistakes more, it helped in revealing whether the model sometimes makes big outlier errors. Finally, R² showed how much of the variation in IMDb ratings can be explained by the features I used compared to a simple baseline. Overall, the regression model performs reasonably well, but there are still some movies where the prediction error is larger, especially for extreme-rated or unusual cases.