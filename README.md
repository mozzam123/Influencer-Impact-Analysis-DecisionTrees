# Instagram Influencers Analysis

## Overview
This project involves analyzing data from top Instagram influencers, focusing on how various factors such as the number of posts, followers, and engagement rates impact their influence score. The objective is to use machine learning to predict the influence score based on the provided features.

## Dataset
The dataset contains information about top Instagram influencers with the following columns:

- **rank**: Rank of the influencer.
- **channel_info**: Username of the influencer.
- **influence_score**: A score representing the overall influence of the account.
- **posts**: Number of posts made by the influencer.
- **followers**: Total number of followers.
- **avg_likes**: Average number of likes per post.
- **60_day_eng_rate**: Engagement rate over the last 60 days.
- **new_post_avg_like**: Average number of likes on recent posts.
- **total_likes**: Total number of likes on all posts.
- **country**: Country of the influencer.


## Steps Performed

1. **Data Preprocessing**:
   - Handled missing values by replacing NaNs in the `country` column with the most frequent value, 'United States'.
   - Removed irrelevant columns like `rank` and `channel_info` for the analysis.
   - Converted string representations of numbers (e.g., 'm' for millions, 'k' for thousands) to actual numeric values.

2. **Feature Selection**:
   - Dropped the `country` column as it had no significant impact on the prediction of the target variable.
   - Chose `influence_score` as the target variable and the rest of the columns as predictors.

3. **Data Normalization**:
   - Applied `StandardScaler` to normalize the predictor variables for better performance of the model.

4. **Train-Test Split**:
   - Divided the dataset into a training set (80%) and a test set (20%).

5. **Model Training**:
   - Used Linear Regression to train the model and predict the influence score.

6. **Evaluation**:
   - Evaluated the model using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared (R²).
   - Visualized the performance by plotting predicted vs actual influence scores.

## Results

### Model Coefficients:
The coefficients of the Linear Regression model reveal that the **followers** feature has the largest positive impact on the influence score.

### Performance Metrics:
- **Mean Absolute Error (MAE)**: The average magnitude of errors between predicted and actual values.
- **Mean Squared Error (MSE)**: The average of squared differences between predicted and actual values.
- **Root Mean Squared Error (RMSE)**: The square root of MSE.
- **R-squared (R²)**: A measure of how well the model's predictions match the actual data.

### Visualization:
Scatter plots comparing predictions with actual values helped assess the accuracy of the model visually.

## Usage

### Prerequisites:
- Python 3.x
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

### Running the Code:
1. Clone the repository and install dependencies:
   ```bash
   pip install -r requirements.txt

