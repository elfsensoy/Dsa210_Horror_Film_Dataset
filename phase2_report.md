# 📌 Phase 2 - Report

This phase covers the data collection, data cleaning steps.

## 🎬 1. Data Collection

I collected horror movies metadata from IMDb (Kaggle) and user reviews from TMDB API.

IMDb Movie Metadata:
* data_raw/Horror Movies IMDb.csv

Contains: title, year, rating, genre, director, votes, runtime.


TMDB User reviews: 
* Raw review data -> data_clean/horror_tmdb_reviews_sample.csv
* Cleaned review data -> data_clean/reviews_tmdb_clean.csv

Contains: Review texts, review ratings, author, date, TMDB ID, movie title & year.
  
Will see how these sets are used in both upcoming phases and in this phase.

## 🧽 2. Data Cleaning & Preparation

All cleaning steps can be found in 01_data_setup.ipynb.

- Standardized column names
- Converted numeric fields. (year, runtime, rating, votes)
- Removed duplicates & missing values.
- Cleaned TMDB review fields. (ratings, dates, text formatting)

Final cleaned files: 
* data_clean/movies_clean.cs
* data_clean/reviews_tmdb_clean.csv

## 📌 3. Exploratory Data Analysis (EDA)
This section provides an initial explotary analysis of both the IMDb movie metadata and the TMDB user review dataset. The goal in this part is to understand the structure of each dataset, identity key patterns.

### 3.1 IMDb Movie Dataset - EDA
I analyzed 836 horror films included in the cleaned IMDb dataset.

Key observations are:
- IMDb Rating Distribution:
Rating follows a roughly normal distribution centered around 6.1, with most movies rated between 5 and 7. 
- Runtime Distribution:
Most films fall within 90-110 minutes, which is typical for the horror genre.
- Yearly Trends:
When grouped by release year, the average IMDb rating differentiates slightly but remains stable over time. As can be seen in the notebool, no strong upward or downward trend is observed.
- Genre Breakdown:
Because IMDb assigns multiple genres per movie, I extracted the primary genre.

The most common primary genres are:
- Horror (frequently, since horror dataset)
- Drama
- Action
- Comedy
  
Which shows that many films mix horror with drama,thriller, or action. 

### 3.2 TMDB User Reviews - EDA
TMDB dataset contains over 2000 reviews for films in our movie list. 

Key observations are:
- Review Rating Distribution:
User rating cluster between 5 and 8, showing slightly positive bias.
Very low (0-2) rating are less frequent.
- Review Lengths:
Review text length is highly skewed.
Most reviews are between 200-600 characters, but a small number exceed 5,000 characters.
- Sentiment Categories:
Based on rating thresholds:
  * Positive (>= 7) - largest group
  * Neutral (5-6)
  * Negative (<5) - smallest group
Which shows us there are more positive reviews on horror movies than negative.

Finnaly the Most reviewd Movies are:
- The Mummy,
- The Psycho,
- Halloween,
- The Predator
- M3GAN



