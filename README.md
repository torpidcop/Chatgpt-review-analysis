# 💬 ChatGPT Reviews: Sentiment & Text Analysis

A Python-based sentiment and text analysis of ChatGPT app reviews, built in Google Colab. The project measures how users feel about the app, how that sentiment compares with their star ratings, and which words and phrases appear most in positive reviews.

---

## 📌 Project Overview

This project applies Natural Language Processing (NLP) to a large set of user reviews. It cleans the raw data, scores each review for **polarity** and **subjectivity**, groups reviews into **positive, neutral and negative** sentiment, and analyzes the language used in positively rated reviews.

## 🎯 Objectives

- Prepare and clean the review data for analysis
- Measure sentiment polarity and subjectivity for each review
- Categorize reviews as positive, neutral or negative and compare them with user ratings
- Identify the most frequently mentioned keywords and phrases in positive reviews
- Visualize sentiment trends, distributions and keyword frequencies

## 📂 Dataset

| Detail | Value |
|---|---|
| File | `chatgpt_reviews.csv` |
| Rows | 196,727 (before cleaning) |
| Period covered | 25 Jul 2023 to 23 Aug 2024 |

| Column | Description |
|---|---|
| `Review Id` | Unique ID of the review |
| `Review` | Text written by the user |
| `Ratings` | Star rating from 1 to 5 |
| `Review Date` | Date and time of the review |

## 🛠️ Tools & Libraries

- **Python** in **Google Colab**
- **pandas, NumPy**: data handling
- **TextBlob**: polarity and subjectivity scoring
- **scikit-learn** (`CountVectorizer`): keyword and phrase frequencies
- **Matplotlib, Seaborn**: charts
- **WordCloud**: word cloud of positive terms

## ⚙️ Project Implementation

### 1. Data Preparation
- Loaded and inspected the dataset
- Standardized column names to snake_case
- Converted the review date to datetime and the rating to a numeric type
- Filled empty reviews and removed duplicate review IDs
- Cleaned the text (lowercase, removed URLs and special characters)

### 2. Sentiment Analysis
- Calculated **polarity** (-1 to +1) and **subjectivity** (0 to 1) with TextBlob
- Categorized reviews: polarity above 0.05 is **Positive**, below -0.05 is **Negative**, and everything else is **Neutral**
- Compared sentiment categories with user star ratings

### 3. Text Analysis
- Filtered positively rated reviews (4 and 5 stars)
- Extracted the most frequent words and two-word phrases
- Visualized the results with frequency bar plots and a word cloud

### 4. Data Visualization
- Sentiment distribution bar chart
- Polarity and subjectivity histograms
- Polarity by rating (box plot) and sentiment mix by rating (stacked bar)
- Monthly review volume and average polarity
