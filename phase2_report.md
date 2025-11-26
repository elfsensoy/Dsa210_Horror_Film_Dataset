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





