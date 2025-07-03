# 🎬 Movie Recommendation System

This project implements a full-fledged **movie recommendation system** using multiple strategies:
- Popularity-based (IMDb-style weighted rating)
- Genre-specific filtering
- Content-based filtering
- Collaborative filtering
- Hybrid approach combining content and user behavior

---

## 🔍 Features

- ✅ **Weighted Rating Algorithm**  
  Uses IMDb-style weighted average to rank popular movies.

- ✅ **Genre-Based Filtering**  
  Generates top movie recommendations within specific genres like Action, Comedy, Drama, etc.

- ✅ **Content-Based Filtering**  
  Recommends similar movies using cosine similarity on TF-IDF vectors built from movie overviews, keywords, and genres.

- ✅ **Collaborative Filtering**  
  Uses matrix factorization (e.g., SVD from the Surprise library) to predict user preferences based on rating patterns.

- ✅ **Hybrid Recommendation Engine**  
  Combines content-based and collaborative filtering results for more accurate, personalized suggestions.

- ✅ **Data Preprocessing & Feature Engineering**  
  Handles nested genre fields, missing data, and feature extraction from metadata.

---

## 📊 Dataset

- **Movies Metadata**
  - Format: `CSV`
  - Source: [Kaggle - TMDB Movie Metadata](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
  - Columns: `title`, `genres`, `overview`, `vote_count`, `vote_average`, `release_date`, `popularity`, etc.

- **Ratings Dataset**
  - Format: `TSV`
  - Columns: `user_id`, `item_id`, `rating`, `timestamp`

---


## ⚙️ Requirements

- **Python 3.8+**
- Required Libraries:
  - `pandas`, `numpy`
  - `matplotlib`, `seaborn`
  - `sklearn`, `scipy`, `ast`, `nltk`

To install all required packages:

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

1. **Clone the repository**:

```bash
git clone https://github.com/your-username/movie-recommendation-system.git
cd movie-recommendation-system
```

2. **Launch the notebook**:

```bash
jupyter notebook movie_recommendation.ipynb
```

3. **Steps inside the notebook**:
   - Load `movies_metadata.csv`
   - Clean and transform the genre data
   - Compute IMDb-style weighted ratings
   - Generate top-rated movies overall or by genre

---

## 📈 Example Results

- **Top 15 Movies (Overall)** based on weighted rating.
- **Top 15 Movies by Genre**:

  Run the function below in the notebook:

  ```python
  build_chart('Action')
  ```

  Replace `'Action'` with any other genre like `'Drama'`, `'Comedy'`, etc.

---

## 📌 Project Workflow

1. **Data Loading**  
   Loads and merges metadata from CSV files.

2. **Data Cleaning**  
   Parses JSON-like genre fields, handles nulls, and converts release dates.

3. **Filtering Logic**  
   Uses a minimum vote count threshold and a weighted formula to rank movies.

4. **Recommendation Output**  
   Sorts top movies globally or within genres.

---

## 🚧 Future Enhancements

- 🌐 Build a user-friendly web interface using **Streamlit** or **Flask**.
- 📡 Fetch real-time data from **TMDB or IMDb APIs**.

---

## 📄 License

This project is licensed under the **MIT License**.
