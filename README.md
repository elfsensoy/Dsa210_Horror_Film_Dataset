# 🎃 Dsa210_Horror_Film_Dataset

**Sabancı University — Introduction to Data Science Project**

---

## 💡 Motivation

Many people love horror movies despite the triggering fear, tension, and discomfort they provide. But not all horror movies succeed in doing so.
This project asks the question:

> *"What makes a horror film truly scary and disturbing?"*

By analyzing the data from audience ratings and reviews, the goal is to uncover cinematic and thematic factors that make some horror movies more terrifying than others.

Understanding this is mostly a personal project of a horror-lover student who gets triggered easily but still watches.
(Also understanding this and seeing the project may help some filmmakers, critics and streaming platforms.)

---

## 📊 Data Sources

This project will mostly rely on publicly available datasets about horror movies from:

* **Kaggle**
* **IMDb Datasets**
* **TMDB API**
  *(May or may not change.)*

---

## 🧠 Data Collection Plan

* Downloading topic-related CSVs from **Kaggle**
* **IMDb API** and **TMDB API** to fetch details
* Merge and clean data using **Python**

---

## ⚙️ Data Analysis Plan

1. **Data Cleaning & Preparation:** Removing duplicates, handling missing values and unifying formats.
2. **Exploratory Data Analysis:** Visualizing rating distributions, sub-genres, and time trends.
3. **Text & Sentiment Analysis:** Extracting emotion and fear-related keywords from user reviews.
4. **Feature Correlation:** Finding relationships between movie characteristics and audience fear perception (from the reviews).
5. **Modeling:** Testing whether certain features can predict a movie's *"scary score."*

---

## 🔍 Expected Findings

Some potential insights include:

* Which sub-genres (psychological, supernatural, slasher) are rated most frightening.
* Which keywords or themes (“death,” “isolation,” “darkness,” etc.) appear most often in highly rated horror films.
* Whether shorter or longer films tend to be scarier.
* How review sentiment correlates with IMDb or audience scores.

---

## ⚠️ Limitations and Future Work

* Audience perception of fear is subjective and depends on culture and individual psychology.
* Online reviews may contain biases (bots, sarcasm, etc.).
* Some data sources (e.g., TMDB API) may have limited access without authentication.

### 🎯 Future Direction

* Expanding analysis to include physiological data (heart rate, EEG) from fear-response studies.
* Build a web app where users can input a movie and see how “scary” it is predicted to be.
* Incorporate machine learning models to classify unseen movies by predicted fear intensity.

---

## 🗓️ Timeline

| **Week** | **Task**             | **Description**                                  |
| -------- | -------------------- | ------------------------------------------------ |
| Week 1   | Data Collection      | Gather and clean horror movie datasets           |
| Week 2   | Exploratory Analysis | Visualize trends, sub-genres, and ratings        |
| Week 3   | Text Analysis        | Perform sentiment and keyword extraction         |
| Week 4   | Modeling             | Correlation or clustering analysis               |
| Week 5   | Results & Report     | Summarize findings in article/video/webpage form |

---

## 🧰 Tools & Libraries

* **Python:** pandas, numpy, matplotlib, seaborn
* **Text Analysis:** nltk, sklearn, wordcloud, transformers (optional)
* **APIs:** IMDb, TMDB
* **Visualization:** Tableau or Matplotlib

