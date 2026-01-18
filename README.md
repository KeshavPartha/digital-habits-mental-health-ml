# Digital Habits vs Mental Health — Machine Learning & Data Analytics Project

## Project Overview
This project analyzes the relationship between **digital habits** (screen time, social media usage, TikTok consumption) and **mental health indicators** with a focus on **stress levels**.

Using an end-to-end **data analytics and machine learning pipeline**, we explore how technology usage affects well-being and whether behavioral data can be used to predict mental health outcomes.

---

## Objectives
- Clean and preprocess real-world behavioral data
- Perform exploratory data analysis (EDA) to reveal trends
- Engineer meaningful behavioral features
- Build and interpret a supervised machine learning model
- Communicate insights on technology’s impact on mental health

---

## Dataset
**Source:** Kaggle — Screen Time Impact on Mental Health by Abhishek Dave

Glimpse of the Dataset:
|   screen_time_hours |   social_media_platforms_used |   hours_on_TikTok |   sleep_hours |   stress_level |   mood_score |
|--------------------:|------------------------------:|------------------:|--------------:|---------------:|-------------:|
|                10.3 |                             2 |               5.3 |           4.4 |             10 |            5 |
|                 6.5 |                             5 |               3.5 |           6.2 |              8 |            8 |
|                 9.1 |                             4 |               2.8 |           6.6 |              7 |            8 |
|                 6.5 |                             3 |               2.5 |           6.5 |              7 |            9 |
|                 2.1 |                             3 |               1.2 |           7.8 |              2 |           10 |

The dataset includes:
- Screen time (hours/day)
- Social media platforms used
- TikTok usage
- Sleep hours
- Mood score
- Stress level (target variable)

---

## Exploratory Data Analysis
EDA revealed strong relationships between **sleep-related variables and stress**, while direct digital usage showed weaker correlations.

Key techniques:
- Distribution analysis
- Pairwise relationships
- Correlation heatmaps
- Behavioral scatter plots

### Correlation Heatmap
<img width="716" height="625" alt="digital_habits_heatmap" src="https://github.com/user-attachments/assets/d9c3d5b2-0379-4fd5-9241-7aade4dbc01c" />

---

## Feature Engineering
To capture behavioral patterns more effectively, the following features were engineered:

- **Sleep Efficiency** = Sleep Hours / Screen Time
- **TikTok Intensity** = TikTok Hours / Screen Time
- **Platform Intensity** = Platforms Used / Screen Time

These features helped model non-linear interactions between digital behavior and mental health.

---

## Machine Learning Model
### **Model Used:** Decision Tree Regressor

The model predicts **stress level** based on digital habits and sleep behavior.

**Why Decision Tree?**
- Handles non-linear relationships
- Works well with small datasets
- Highly interpretable
- No feature scaling required

---

## Model Performance
- **R² Score:** ~0.70  
- **RMSE:** Low error on stress level scale (1–10)

### Interpretation:
- ~70% of the variation in stress level is explained by behavioral data
- Strong predictive power for a mental-health-related dataset

---

## Feature Importance
<img width="1028" height="451" alt="Feature_Importance" src="https://github.com/user-attachments/assets/6e2975e5-02af-46a8-ac3d-8792182cd897" />


**Key Insight:**  
Sleep efficiency and sleep duration dominate stress prediction, while direct digital usage plays a smaller role.

---

## Key Findings
- Poor sleep relative to screen time strongly increases stress
- Sleep quality matters more than total screen time
- Digital habits affect mental health indirectly through sleep
- Machine learning can uncover behavioral patterns in mental health data

---

## Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Google Colab

---

## Future Improvements
- Compare with Linear Regression and Neural Networks
- Add cross-validation and hyperparameter tuning
- Predict mood score as a secondary target
- Expand dataset with demographic or longitudinal data

