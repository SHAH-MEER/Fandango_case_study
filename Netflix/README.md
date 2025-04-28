# Netflix Titles Exploratory Data Analysis (EDA)

This project provides an in-depth exploratory data analysis (EDA) of the Netflix Titles dataset. The analysis uncovers trends, patterns, and insights about the content available on Netflix, including movies and TV shows from around the world.

## Dataset
- **Source:** [Kaggle - Netflix Shows Dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **File:** `DATA/netflix_titles.csv`
- **Description:** Contains detailed information about Netflix titles, such as title, type, director, cast, country, date added, release year, rating, duration, genres, and description.

## Key Analysis Steps
- Data cleaning and handling of missing values
- Feature engineering (e.g., number of actors, genres, duration extraction)
- Visualizations: content type, ratings, country & genre distributions, trends over time
- Advanced analyses: actor/director networks, clustering with K-Means, PCA/t-SNE visualizations

## Notable Insights
- The United States and India are the largest contributors of content.
- Dramas, International Movies, and Comedies are the most common genres.
- Most movies have a duration of 80–120 minutes; most TV shows have 1–2 seasons.
- Distinct clusters of content types and collaborative networks among actors/directors were identified.

## Directory Structure
```
Netflix/
│
├── DATA/
│   └── netflix_titles.csv
├── visualisations/
│   └── ... (generated plots)
├── Netflix-Titles.ipynb
└── README.md
```

## Credits
- Dataset by [shivamb](https://www.kaggle.com/datasets/shivamb/netflix-shows) on Kaggle.
- Analysis and notebook by [Your Name].

---

Feel free to extend this analysis or use the code as a template for exploring similar datasets!
