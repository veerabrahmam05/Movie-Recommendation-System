# 🎬 Movie Recommendation System

This project implements a **popularity-based** and **genre-specific movie recommendation system** using movie metadata from TMDB. It filters and ranks movies based on vote count, average rating, and genre using an IMDb-style weighted formula.

---

## 🔍 Features

- ✅ **Weighted Rating Algorithm**  
  Recommends movies using an IMDb-style weighted formula combining vote average and vote count.

- ✅ **Genre-Based Filtering**  
  Generates top movie recommendations by specific genres like Action, Comedy, Drama, etc.

- ✅ **Data Preprocessing & Feature Engineering**  
  Cleans and transforms complex nested genre data using `ast.literal_eval`.

- ✅ **(Optional) Data Visualization**  
  Can be extended to visualize trends using Seaborn and Matplotlib.

---

## 📊 Dataset

- **Movies Metadata**
  - Format: `CSV`
  - Source: [Kaggle - TMDB Movie Metadata](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
  - Key Columns: `title`, `genres`, `vote_count`, `vote_average`, `release_date`, `popularity`, etc.

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

- 🔄 Integrate **collaborative filtering** using Surprise or LightFM.
- 🤝 Combine **content-based and collaborative methods** (hybrid model).
- 🌐 Build a user-friendly web interface using **Streamlit** or **Flask**.
- 📡 Fetch real-time data from **TMDB or IMDb APIs**.

---

## 📄 License

This project is licensed under the **MIT License**.
