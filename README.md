# Sentiment-Based Drug Recommender System

## Overview
This project is a sentiment-based drug recommender system built using a dataset of drug reviews. The system helps identify the top drugs for various medical conditions based on user reviews, ratings, and useful counts. It leverages Natural Language Processing (NLP) techniques and machine learning models to predict sentiment and rank drugs based on composite scores.

## Dataset
The dataset is composed of drug reviews with the following columns:
- **uniqueID:** Unique identifier for each review
- **drugName:** Name of the drug
- **condition:** Medical condition the drug is used for
- **review:** Textual review of the drug by a user
- **rating:** Numerical rating of the drug (1-10)
- **date:** Date the review was submitted
- **usefulCount:** Number of users who found the review helpful

## Key Features
- **Sentiment Analysis:** Predict the sentiment (positive or negative) of drug reviews.
- **Composite Score Calculation:** Create a composite score based on the rating, sentiment, and useful count.
- **Drug Ranking:** Rank drugs for each condition based on their composite scores.
- **Exploratory Data Analysis (EDA):** Insights into the most common conditions, drug names, and distributions.
- **Word Clouds:** Visualize common words in high-rated and low-rated reviews.

## Models Used
- **LSTM Neural Network:** A recurrent neural network model used for sentiment classification of reviews.
- **LightGBM:** A gradient boosting framework used for sentiment prediction using TF-IDF features.

## Libraries
- **pandas:** For data manipulation and analysis.
- **numpy:** For numerical operations.
- **seaborn, matplotlib:** For data visualization.
- **sklearn:** For machine learning preprocessing and evaluation.
- **tensorflow:** For building the LSTM neural network.
- **lightgbm:** For the LightGBM model.
- **wordcloud:** For generating word cloud visualizations.
- **nltk:** For text preprocessing.
- **skimpy:** For summarizing the dataset.

## Installation
To install the required dependencies, run:
```bash
pip install -r requirements.txt
Usage
Data Preprocessing

Run the script to clean and preprocess the data. This includes:
Removing inappropriate values (e.g., HTML tags from scraped reviews).
Filling missing values using group-based strategies.
Cleaning text by removing URLs, emojis, and punctuation.
Training the Sentiment Classifier

Use the LSTM model to classify reviews into positive or negative sentiment. Alternatively, you can use the LightGBM model based on TF-IDF vectorized features.
Ranking Drugs

The script calculates composite scores for each drug and ranks them within each condition.
Visualizations

Generate visualizations such as:
Bar plots for the most common conditions and drugs.
Pie charts for distribution of conditions.
Word clouds for common words in high-rated and low-rated reviews.
Output

The top-ranked drugs for each condition are stored in a CSV file, and visualizations are saved as images.
