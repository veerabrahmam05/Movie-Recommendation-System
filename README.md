Movie Recommendation System

This project implements a collaborative filtering-based movie recommendation system using user rating data. It analyzes user behavior to recommend movies based on similarity in ratings and popularity.

Features

Collaborative Filtering: Recommends movies by analyzing user rating patterns.

Statistical Insights: Calculates average ratings and the number of ratings per movie for better recommendations.

Data Visualization: Visualizes trends in user ratings distribution using Seaborn and Matplotlib.

Dataset

Movie Ratings Data:

Format: Tab-separated values (.tsv).

Columns: user_id, item_id, rating, timestamp.

Movie Titles:

Format: CSV.

Columns: item_id, title.

Prerequisites

Python 3.8+

Libraries:

pandas, numpy: Data manipulation.

matplotlib, seaborn: Data visualization.

Installation

Clone the repository:

    git clone https://github.com/your-username/movie-recommendation-system.git
    cd movie-recommendation-system
    
Install dependencies:

    pip install -r requirements.txt
    
Place the datasets (file.tsv and Movie_Id_Titles.csv) in the working directory.

Usage

Open the Python script or Jupyter Notebook:

    jupyter notebook movie_recommendation.ipynb
    
Follow these steps in the code:

Load and merge the datasets.

Visualize data trends (e.g., rating distributions).

Compute correlations for movies based on user ratings.

Filter recommendations by rating popularity.

Project Workflow

Data Loading:

Merges ratings and movie titles using the item_id.

Data Analysis:

Calculates average movie ratings.

Counts the number of ratings for each movie.

Recommendation:

Computes pairwise correlations between movies.
Filters recommendations to include movies with at least 100 ratings for reliability.

Results

Popular Movies: Identifies movies with the highest ratings and most reviews.

Recommendations: Recommends movies similar to a selected one (e.g., Star Wars (1977) or Liar Liar (1997)).

Future Enhancements

Integrate a user interface for easier interaction.

Expand to include content-based filtering.

Fetch live data from online APIs like TMDB or IMDb.
