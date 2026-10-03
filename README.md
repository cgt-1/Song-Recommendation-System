# Song-Recommendation-System
A content-based song recommendation system built using a Spotify dataset. The project covers data preprocessing, exploratory data analysis, feature engineering, and song similarity using audio features and genres.

## 📌 Overview

The notebook first cleans and explores the dataset by handling:

- Missing values
- Duplicate songs
- Numerical outliers
- Inconsistent genre formatting

The recommender then represents each song using its **audio features and genres**. These features are combined into a single representation, and **cosine similarity** is used to find the most similar songs.

## 🎧 Recommendation Approach

- **StandardScaler** — standardizes numerical audio features such as tempo, energy, and danceability so features with larger numerical ranges do not dominate similarity calculations.
- **MultiLabelBinarizer** — converts multiple genres into multi-hot encoded vectors. For example, `['pop', 'dance pop']` becomes binary genre features.
- **TF-IDF** — gives more weight to distinctive genre terms while reducing the influence of very common genres.
- **hstack** — combines the different feature representations into one sparse feature matrix.
- **Cosine Similarity** — measures how similar two songs are based on their overall feature profiles and returns the top-N recommendations.

## 📊 Exploratory Data Analysis

The notebook includes:

- Popularity distribution
- Numerical feature boxplots
- Audio feature correlation heatmap
- Genre frequency and distribution analysis

## 🛠️ Tech Stack

- **Python**
- **pandas & NumPy** — data processing
- **Matplotlib & Seaborn** — visualization
- **scikit-learn** — `StandardScaler`, `MultiLabelBinarizer`, `TfidfVectorizer`, and `cosine_similarity`
- **SciPy** — sparse matrix operations with `hstack`

## 📁 Project Structure

```text
Song-Recommendation/
├── SongReccomendationSystem.ipynb
└── song_recomendation_A.csv
