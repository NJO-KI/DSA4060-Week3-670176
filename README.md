# DSA 4060 - Week 3 Practical Lab: Building a Simple Content-Based Recommender

## Overview
This repository contains the implementation for the DSA 4060 Week 3 Practical Lab on Content-Based Recommender Systems. The project demonstrates a content-based filtering workflow using structured binary genre features, pandas, and Python.

## Objectives
- Represent movie items using structured binary feature vectors.
- Construct an item-feature matrix.
- Generate normalized user preference profiles from historical ratings.
- Calculate candidate movie scores using weighted feature aggregation.
- Filter out previously watched items and output Top-N recommendations.
- Evaluate model limitations and edge cases (such as the cold-start problem and filter bubbles).

## Repository Structure
```
DSA4060-Week3/
├── content_based_lab.ipynb
├── README.md
└── movies.csv
```

## Dataset Description
The catalog consists of 10 initial movies encoded with 5 binary genre attributes (`Action`, `Comedy`, `Drama`, `Romance`, `SciFi`).

- `movie_id`: Unique identifier for each movie.
- `title`: String name of the movie.
- `Action`, `Comedy`, `Drama`, `Romance`, `SciFi`: Binary indicators where `1` indicates the presence of a genre feature and `0` indicates absence.

## Workflow Summary
1. **Item Profiles**: Represent candidate movies using structured feature vectors.
2. **User Ratings**: Join user interaction history with movie features.
3. **Weighting**: Multiply feature vectors by ratings given by the user.
4. **User Profile**: Sum and normalize weighted features into a proportion vector summing to 1.0.
5. **Scoring**: Compute preference scores across the full movie catalog using dot-product multiplication.
6. **Filtering**: Exclude movies already present in the user's rating history.
7. **Ranking**: Sort candidate movies by recommendation score to output the Top-N recommendations.

## Usage
To run the notebook locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/DSA4060-Week3.git
   ```
2. Navigate to the project directory:
   ```bash
   cd DSA4060-Week3
   ```
3. Open and run the Jupyter Notebook:
   ```bash
   jupyter notebook content_based_lab.ipynb
   ```

## Dependencies
- Python 3.x
- pandas
