# Social-Media-Engagement

# 📊 Social Media Engagement Prediction

This project analyzes and predicts user engagement on social media posts using post metadata. It explores how various factors such as platform, post type, sentiment, and time of posting influence two key engagement metrics: **likes** and **comments**.

## 🚀 Project Goals

- Analyze patterns in social media engagement across different platforms and post types
- Explore time-based trends (e.g., by hour, day of the week)
- Build a **multi-output regression model** to predict:
  - Number of likes
  - Number of comments
- Identify which features most impact engagement
- Discuss challenges and potential improvements

## 🧠 Key Insights

- **Likes** were predicted with high accuracy (R² ≈ 0.97), suggesting metadata features are good indicators.
- **Comments** were more difficult to predict (R² ≈ 0.26), likely due to missing context (e.g., content quality, controversial topics).
- Time of day and day of week showed clear engagement trends, particularly around midnight and weekdays.

## 📂 Dataset

The dataset includes 100 social media posts with the following features:
- `platform` (e.g., Facebook, Twitter, Instagram)
- `post_type` (e.g., image, video, poll)
- `likes`, `comments`, `shares`
- `sentiment_score` (positive, neutral, negative)
- `date`, `time` of post

> Note: Post content and user data were not included, limiting predictive accuracy for comments.

## 🛠️ Tools & Technologies

- **Python (Pandas, NumPy)** – Data processing & feature engineering  
- **Matplotlib, Seaborn** – Visualization  
- **Scikit-learn** – Model building & evaluation  
- **RandomForestRegressor** within `MultiOutputRegressor` for multi-target prediction

## 📈 Model Performance

| Target   | MAE   | RMSE  | R² Score |
|----------|-------|-------|----------|
| Likes    | ~172  | ~239  | 0.97     |
| Comments | ~109  | ~127  | 0.26     |

## 📌 Limitations

- Small dataset (100 rows), limiting generalizability
- No text/content features, which could significantly improve comment predictions
- Sentiment score was not used as a feature in modeling but could be in future versions

## ✅ Next Steps

- Incorporate NLP features from post content (e.g., text length, keywords, tone)
- Test with a larger dataset
- Try other model types (e.g., XGBoost, Gradient Boosting)
- Add engagement prediction for
