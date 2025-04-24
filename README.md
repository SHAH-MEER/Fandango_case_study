# 🎬 Behind the Stars: Analyzing Fandango's Rating System 🌟

This project investigates potential bias in Fandango's movie ratings by analyzing their 2015 rating system. The analysis is based on the FiveThirtyEight article ["Be Suspicious Of Online Movie Ratings, Especially Fandango's"](https://fivethirtyeight.com/features/fandango-movies-ratings/).

## 🔍 Project Overview

The investigation examines if Fandango's ratings had a systematic bias toward inflating movie scores to potentially drive ticket sales. The analysis focuses on:

1. Comparing Fandango's displayed ratings with their actual underlying user ratings
2. Analyzing the distribution of rating differences
3. Comparing Fandango's ratings with other major platforms (Rotten Tomatoes, Metacritic, IMDb)
4. Identifying patterns of systematic bias in the rating system

## 📊 Datasets

The project uses two main datasets from FiveThirtyEight's GitHub repository:

### 1. `fandango_scrape.csv`

Contains Fandango's movie ratings with the following columns:
- `FILM`: Movie title and year
- `STARS`: Number of stars displayed on Fandango.com
- `RATING`: Actual average rating value from the HTML
- `VOTES`: Number of user reviews

### 2. `all_sites_scores.csv`

Contains aggregated ratings from multiple platforms:
- `FILM`: Movie title
- `RottenTomatoes`: Tomatometer score
- `RottenTomatoes_User`: User score
- `Metacritic`: Critic score
- `Metacritic_User`: User score
- `IMDB`: User score
- `Metacritic_user_vote_count`: Number of Metacritic user votes
- `IMDB_user_vote_count`: Number of IMDb user votes

## 📈 Analysis Methodology

The analysis follows these steps:

### 1. Data Exploration
- Load and examine both datasets
- Clean and prepare the data
- Calculate basic statistics

### 2. Fandango Rating Analysis
- Compare displayed stars vs. actual ratings
- Calculate rating differences
- Analyze rating distributions
- Identify potential rounding or display biases

### 3. Cross-Platform Comparison
- Merge datasets for movies present in both
- Compare Fandango ratings with other platforms
- Calculate correlations between different rating systems
- Identify systematic differences

### 4. Visualization
- Create distribution plots of rating differences
- Generate correlation heatmaps
- Visualize rating comparisons across platforms

## 💡 Key Findings

The analysis reveals:

1. Discrepancies between Fandango's displayed ratings and actual user ratings
2. Systematic differences in how Fandango rates movies compared to other platforms
3. Potential bias in the rating display system
4. Patterns in rating distributions that suggest intentional inflation

## 🛠️ Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/SHAH-MEER/fandango_case_study.git
   cd fandango_case_study
   ```

2. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the analysis:
   ```bash
   jupyter notebook fandango_case_study.ipynb
   ```

## 📁 Project Structure

```
fandango_case_study/
├── fandango_case_study.ipynb   # Main analysis notebook
├── requirements.txt            # Project dependencies
├── README.md                   # This file
├── data/                       # Data directory
│   ├── fandango_scrape.csv     # Fandango ratings data
│   └── all_sites_scores.csv    # Cross-platform ratings data
└── visualizations/             # Generated visualization files
    ├── rating_differences.png
    ├── correlation_heatmap.png
    └── platform_comparison.png
```

## 🙏 Acknowledgments

- FiveThirtyEight for the original article and data
- Walt Hickey for the original analysis