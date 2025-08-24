Task 2 - Sentiment Analysis 
# Sentiment Analysis Report
## 1. Problem Statement

In today’s digital world, social media platforms generate vast amounts of user opinions daily. Understanding these opinions is crucial for businesses, policymakers, and researchers to gauge public perception. This project focuses on performing sentiment analysis on tweets to categorize them into positive, negative, or neutral sentiments and identify the most frequent words associated with each sentiment.

## 2. Overview

The objective of this project is to analyze tweets, classify them based on sentiment, and visualize the common keywords using word clouds and statistical techniques. By doing so, we can uncover insights about public opinion and identify patterns in online discussions.

## 3. Tools and Frameworks Used

Python Libraries

pandas → for data preprocessing and cleaning

matplotlib & seaborn → for visualization

WordCloud → for generating word clouds

VADER (Valence Aware Dictionary for Sentiment Reasoning) → for sentiment classification

Dataset

CSV file containing tweets and sentiment labels.

## 4. Methodology

Data Cleaning: 
Removed missing values and ensured only valid text entries were analyzed.

Sentiment Classification:
Used VADER sentiment analyzer to classify text into Positive, Negative, and Neutral categories.

Visualization:
1.Plotted distribution of sentiments.
2.Generated word clouds to represent frequent words in each sentiment category.

Top Word Extraction: 
Identified top 10 words for each sentiment.

## 5. Results & Insights

Most tweets were positive, showing an overall optimistic sentiment trend.

Positive tweets focused on words like love, great, good, thanks.

Negative tweets were dominated by words such as bad, hate, problem, worst.

Neutral tweets contained general words with less emotional intensity.

Word clouds visually confirmed the dominance of sentiment-driven keywords.

## 6. Applications

Business: Analyzing customer feedback and product reviews.

Politics: Understanding public opinion on policies.

Healthcare: Monitoring mental health trends in social media discussions.

Marketing: Identifying customer preferences and brand perception.

## 7. Conclusion

This project successfully demonstrated how sentiment analysis can extract meaningful insights from social media data. The combination of VADER sentiment analysis, visualization techniques, and word frequency analysis provided a clear understanding of the dataset.
Overall, the analysis revealed that positive sentiments outweighed negative ones, indicating a generally favorable online environment in the dataset.

