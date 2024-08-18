# Namma Yatri App Review Analysis

## Overview

This project presents a comprehensive analysis of 11,174 user reviews of the Namma Yatri app. The goal was to uncover insights related to user sentiment, identify key areas for improvement, and evaluate the app's performance across different versions. Various techniques including sentiment analysis, topic modeling, and machine learning were applied to extract meaningful patterns and trends from the reviews.

## Table of Contents

- [Data Understanding and Preprocessing](#data-understanding-and-preprocessing)
- [Sentiment Analysis](#sentiment-analysis)
- [App Version Analysis](#app-version-analysis)
- [Feature Extraction and Clustering](#feature-extraction-and-clustering)
- [Machine Learning Models](#machine-learning-models)
- [Topic Modeling](#topic-modeling)
- [Conclusions and Insights](#conclusions-and-insights)
- [Strategic Recommendations](#strategic-recommendations)
- [How to Use](#how-to-use)
- [License](#license)

## Data Understanding and Preprocessing

The dataset contains 11,174 reviews with key columns such as `reviewId`, `userName`, `content`, `score`, `thumbsUpCount`, `reviewCreatedVersion`, and `appVersion`. Missing values were addressed, and text preprocessing included steps like lowercasing, removing special characters and stopwords, and tokenization.

## Sentiment Analysis

Sentiment analysis was conducted using three methods: VADER, TextBlob, and a Custom Model. The results consistently showed a majority of positive sentiment across the reviews. Here's a summary of the sentiment distribution:

- **Positive**: 60.91% (VADER), 66.11% (TextBlob), 64.60% (Custom Model)
- **Negative**: 23.91% (VADER), 19.34% (TextBlob), 35.27% (Custom Model)
- **Neutral**: 15.18% (VADER), 14.55% (TextBlob), 0.13% (Custom Model)

## App Version Analysis

Analysis of app versions showed that newer versions generally received higher ratings, indicating improvements in user satisfaction. Key insights include:

- **Version 1.1.2**: Perfect 5.0 rating (potentially due to a small sample size).
- **Versions 1.2.2 and 1.3.3**: Peaks in user satisfaction.
- **Recent versions (2.5.7 and 2.5.8)**: Slightly lower ratings compared to some earlier versions.

## Feature Extraction and Clustering

Top features extracted using TF-IDF include:

1. "good" (13.43%)
2. "app" (6.55%)
3. "nice" (3.30%)
4. "service" (3.18%)
5. "ride" (2.65%)

KMeans clustering revealed five main clusters related to service quality, overall app experience, comparisons with competitors, app functionality, and specific ride issues.

## Machine Learning Models

Several machine learning models were trained to predict user sentiment. The Neural Network model achieved the highest accuracy at 87%. Here are the performance metrics for each model:

| Model           | Accuracy | Precision | Recall   | F1 Score | ROC AUC  |
|-----------------|----------|-----------|----------|----------|----------|
| Naive Bayes     | 0.744966 | 0.718904  | 0.744966 | 0.719395 | 0.895247 |
| SVM             | 0.786130 | 0.798383  | 0.786130 | 0.790054 | 0.920176 |
| Random Forest   | 0.791499 | 0.804235  | 0.791499 | 0.795780 | 0.924787 |
| Neural Network  | 0.870246 | 0.854380  | 0.870246 | 0.861310 | N/A      |
| Logistic Reg.   | 0.793736 | 0.716138  | 0.793736 | 0.734176 | N/A      |

## Topic Modeling

LDA topic modeling identified five main topics within the reviews:

1. **App Functionality and Ride Experience**: "app", "ride", "auto", "drivers", "time", "worst", "cancel"
2. **Positive Reviews and Service Quality**: "service", "good", "namma", "app", "yatri", "super", "best"
3. **Driver and Fare Issues**: "driver", "app", "location", "drivers", "auto", "extra", "fare"
4. **Customer Support and App Issues**: "nice", "app", "customer", "support", "high", "otp", "response"
5. **Comparison of Ride-Hailing Services**: "good", "ola", "uber", "app", "price", "better", "compared"

## Conclusions and Insights

1. **Overall Positive Sentiment**: Over 60% positive reviews across all sentiment analysis methods.
2. **Key Strengths**: Overall app quality, service, and ride experience.
3. **Areas for Improvement**:
   - Driver behavior and fare issues
   - App functionality (location services, OTP)
   - Customer support enhancement
4. **Competitive Landscape**: Frequent comparisons with Ola and Uber.
5. **Version Impact**: No clear trend, but certain updates (1.2.2, 1.3.3) were well-received.
6. **Developer Responsiveness**: Active engagement with user feedback, especially negative reviews.
7. **Predictive Modeling**: High performance of the Neural Network model (87% accuracy).
8. **Topic Diversity**: Five main topics provide a comprehensive view of user experience.

## Strategic Recommendations

1. **Product Development**: Improve app functionality, especially location services and payment systems.
2. **Driver Management**: Enhance driver behavior and reliability.
3. **Pricing Strategy**: Review fare structures to address user concerns while maintaining competitiveness.
4. **Customer Support**: Strengthen support systems, particularly for emergencies and quick issue resolution.
5. **Marketing**: Leverage strengths in service quality and overall experience for differentiation.
6. **User Engagement**: Expand practice of responding to user reviews, focusing on constructive feedback.

## How to Use

Clone this repository and explore the various notebooks and scripts provided to understand the analysis process and replicate the results.

# Run this command in command promt
git clone https://github.com/yourusername/namma_yatri_reviews_analysis.git
cd namma_yatri_reviews_analysis
