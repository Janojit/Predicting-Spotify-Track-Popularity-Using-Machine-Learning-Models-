# Predicting Spotify Track Popularity Using Machine Learning Models

## Abstract
This study explores the application of various machine learning models to predict the popularity of music tracks on Spotify. Using a comprehensive dataset of track features, we implemented and compared multiple regression models, including traditional algorithms and advanced ensemble techniques. The research demonstrates that ensemble methods, particularly the Voting Regressor, achieve the best performance with a testing R² value of approximately 0.43. The study provides insights into the relationship between audio features and track popularity, offering valuable implications for music industry stakeholders.

## Introduction

### Background
The music streaming industry has transformed how people consume music, with Spotify being one of the leading platforms. Understanding what makes a track popular has become crucial for artists, producers, and music industry professionals.

### Motivation
The ability to predict track popularity based on audio features can help:
- Artists and producers in optimizing their music for better audience reception
- Music platforms in improving recommendation systems
- Record labels in identifying potential hit songs

### Objectives
- Develop machine learning models to predict track popularity using audio features
- Compare the effectiveness of different modeling approaches
- Identify the most influential factors affecting track popularity

## Dataset Description

### Source
The dataset was obtained from the "https://huggingface.co/datasets/maharshipandya/spotify-tracks-dataset" collection.

### Features
The dataset includes various audio features:
- Duration
- Danceability
- Energy
- Key
- Loudness
- Speechiness
- Acousticness
- Instrumentalness
- Liveness
- Valence
- Tempo
- Mode
- Explicit (boolean)
- Track genre

### Target Variable
The target variable is 'popularity', representing a track's popularity score on Spotify.

## Data Preprocessing

### Data Cleaning
- Removed duplicate entries
- Handled missing values by dropping them (justified by the small number of null values)
- Converted 'explicit' feature to integer type

### Feature Engineering
- Implemented target encoding for the 'track_genre' feature due to its high cardinality
- Maintained original features without removing outliers to preserve valuable information about unique tracks

### Feature Scaling
- Applied StandardScaler to features with Gaussian-like distributions
- Used MinMaxScaler for bounded features (key, tempo)
- Created encoded versions of categorical variables

## Methodology

### Base Models
1. Linear Regression
2. Ridge Regression
3. Lasso Regression
4. Decision Tree
5. Random Forest
6. Gradient Boosting
7. XGBoost
8. K-Nearest Neighbors
9. Support Vector Regression

### Ensemble Models
1. Voting Regressor
2. Stacking Regressor
3. Bagging Regressor
4. Gradient Boosting Regressor
5. AdaBoost Regressor

### Advanced Neural Ensemble Models
1. Basic Neural Ensemble
2. Neural Ensemble with Cross-Validation

## Implementation

### Tools and Libraries
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

### Training Process
- Split data into 80% training and 20% testing sets
- Implemented GridSearchCV for hyperparameter tuning

## Results

### Model Performance Comparison
Best performing model based on Testing R²:
Voting Regressor (R² ≈ 0.43)

### Error Metrics
- MAE and MSE values show consistent patterns with R² scores
- Ensemble methods generally outperformed individual models
- Neural ensemble models showed competitive performance but with signs of overfitting

## Discussion

### Model Performance Analysis
- Voting Regressor showed the best balance between training and testing performance
- Random Forest and Neural Ensemble exhibited overfitting tendencies
- AdaBoost and SVR showed signs of underfitting

### Limitations
- High cardinality in categorical features required special handling
- Some models showed significant overfitting despite regularization
- The relationship between audio features and popularity might be more complex than captured by current models

## Conclusion

### Key Findings
1. Ensemble methods, particularly the Voting Regressor, provide the most reliable predictions
2. Audio features alone can explain approximately 49% of the variance in track popularity
3. Complex models tend to overfit, suggesting the need for careful regularization

### Future Work
- Investigate additional feature engineering techniques
- Explore deep learning approaches
- Incorporate temporal features to capture trends
- Consider including artist and album popularity metrics

## Contributors

- **Janojit Chakraborty** - [GitHub: Janojit](https://github.com/Janojit)
- **Supriya Dutta**

## Contact

For any questions, feedback, or support, please reach out to the project maintainer:

- **Janojit Chakraborty**:
  - **LinkedIn**: [Janojit Chakraborty](https://www.linkedin.com/in/janojit-chakraborty-a50a25235/)

---
