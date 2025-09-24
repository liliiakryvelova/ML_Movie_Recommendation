# Dataset Files - MovieLens Data

## Important Note About Data Files

The original CSV data files (`movie.csv` and `rating.csv`) from the MovieLens dataset are not included in this repository due to file size constraints and GitHub storage limits.

## How to Get the Data

### Option 1: Download from MovieLens (Recommended)
1. Visit: https://grouplens.org/datasets/movielens/
2. Download the MovieLens 100K or Latest dataset
3. Extract the files to the `archive/` directory
4. Ensure files are named:
   - `movie.csv` (or `movies.csv`)
   - `rating.csv` (or `ratings.csv`)

### Option 2: Sample Data for Testing
If you just want to test the notebook functionality, you can create minimal sample files:

```python
# Create minimal sample data for testing
import pandas as pd

# Sample movies
movies_data = {
    'movieId': [1, 2, 3, 4, 5],
    'title': ['Toy Story (1995)', 'Jumanji (1995)', 'Grumpier Old Men (1995)', 
              'Waiting to Exhale (1995)', 'Father of the Bride Part II (1995)'],
    'genres': ['Adventure|Animation|Children|Comedy|Fantasy', 
               'Adventure|Children|Fantasy', 'Comedy|Romance', 
               'Comedy|Drama|Romance', 'Comedy']
}

# Sample ratings
ratings_data = {
    'userId': [1, 1, 1, 2, 2, 2, 3, 3, 3],
    'movieId': [1, 2, 3, 1, 2, 4, 1, 3, 5],
    'rating': [4.0, 3.5, 4.0, 5.0, 3.0, 4.5, 3.5, 4.0, 2.5],
    'timestamp': [964982703, 964981247, 964982224, 964982931, 
                  964982400, 964983815, 964982931, 964981208, 964982176]
}

# Save to CSV
pd.DataFrame(movies_data).to_csv('archive/movie.csv', index=False)
pd.DataFrame(ratings_data).to_csv('archive/rating.csv', index=False)
```

### File Structure Expected
```
archive/
├── movie.csv      # Movie metadata (movieId, title, genres)
└── rating.csv     # User ratings (userId, movieId, rating, timestamp)
```

## Dataset Information

- **Source**: GroupLens Research (University of Minnesota)
- **License**: Use permitted for academic and research purposes
- **Size**: Varies by dataset version (100K to 25M+ ratings)
- **Content**: User ratings, movie metadata, genre information

## For Capstone Evaluation

Evaluators can:
1. Download the public MovieLens dataset as described above
2. Use the sample data generator provided
3. Focus on the algorithm implementations and analysis rather than raw data

The core capstone contributions (research analysis, algorithm implementations, documentation) are fully contained in this repository and do not require the original data files.
