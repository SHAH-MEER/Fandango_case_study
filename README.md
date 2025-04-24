# Behind the Stars: Analyzing Fandango's Rating System

This project investigates potential bias in Fandango's movie ratings by analyzing their 2015 rating system. The goal is to determine if Fandango's ratings had a systematic bias towards rating movies better to sell more tickets.

## Project Overview

The analysis is based on the FiveThirtyEight article ["Be Suspicious Of Online Movie Ratings, Especially Fandango's"](http://fivethirtyeight.com/features/fandango-movies-ratings/). The investigation focuses on:

1. Comparing Fandango's displayed ratings with their actual user ratings
2. Analyzing the distribution of rating differences
3. Comparing Fandango's ratings with other major platforms (Rotten Tomatoes, Metacritic, IMDb)
4. Identifying potential systematic bias in the rating system

The goal is to determine if Fandango's ratings in 2015 had a bias towards rating movies better to sell more tickets, using data analysis and visualization techniques.

## Dataset

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

## Analysis Methodology

The analysis follows these steps:

1. **Data Exploration**
   - Load and examine both datasets
   - Clean and prepare the data
   - Calculate basic statistics

2. **Fandango Rating Analysis**
   - Compare displayed stars vs. actual ratings
   - Calculate rating differences
   - Analyze rating distributions
   - Identify potential rounding or display biases

3. **Cross-Platform Comparison**
   - Merge datasets for movies present in both
   - Compare Fandango ratings with other platforms
   - Calculate correlations between different rating systems
   - Identify systematic differences

4. **Visualization**
   - Create distribution plots of rating differences
   - Generate correlation heatmaps
   - Visualize rating comparisons across platforms

## Setup

1. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the analysis:
```bash
python movie_ratings_analysis.py
```

## Project Structure

- `movie_ratings_analysis.py` - Main analysis script
- `requirements.txt` - Project dependencies
- `data/` - Directory containing the datasets
  - `fandango_scrape.csv`
  - `all_sites_scores.csv`
- `*.png` - Generated visualization files

## Key Findings

The analysis reveals:
1. Discrepancies between Fandango's displayed ratings and actual user ratings
2. Systematic differences in how Fandango rates movies compared to other platforms
3. Potential bias in the rating display system
4. Patterns in rating distributions that suggest intentional inflation