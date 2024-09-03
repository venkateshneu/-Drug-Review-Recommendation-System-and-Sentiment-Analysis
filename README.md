Overview
This project is a sentiment-based drug recommender system built using a dataset of drug reviews. The system helps identify the top drugs for various medical conditions based on user reviews, ratings, and useful counts. It leverages Natural Language Processing (NLP) techniques and machine learning models to predict sentiment and rank drugs based on composite scores.

Dataset
The dataset is composed of drug reviews with the following columns:

uniqueID: Unique identifier for each review
drugName: Name of the drug
condition: Medical condition the drug is used for
review: Textual review of the drug by a user
rating: Numerical rating of the drug (1-10)
date: Date the review was submitted
usefulCount: Number of users who found the review helpful
Key Features
Sentiment Analysis: Predict the sentiment (positive or negative) of drug reviews.
Composite Score Calculation: Create a composite score based on the rating, sentiment, and useful count.
Drug Ranking: Rank drugs for each condition based on their composite scores.
Exploratory Data Analysis (EDA): Insights into the most common conditions, drug names, and distributions.
Word Clouds: Visualize common words in high-rated and low-rated reviews.

Models Used
LSTM Neural Network: A recurrent neural network model used for sentiment classification of reviews.
LightGBM: A gradient boosting framework that was used for sentiment prediction using TF-IDF features.
Libraries
pandas: For data manipulation and analysis.
numpy: For numerical operations.
seaborn, matplotlib: For data visualization.
sklearn: For machine learning preprocessing and evaluation.
tensorflow: For building the LSTM neural network.
lightgbm: For the LightGBM model.
wordcloud: For generating word cloud visualizations.
nltk: For text preprocessing.
skimpy: For summarizing the dataset.
Installation
To install the required dependencies, run:

bash
Copy code
pip install -r requirements.txt
Usage
1. Data Preprocessing
Run the script to clean and preprocess the data. This includes:

Removing inappropriate values (e.g., HTML tags from scraped reviews).
Filling missing values using group-based strategies.
Cleaning text by removing URLs, emojis, and punctuation.
2. Training the Sentiment Classifier
Use the LSTM model to classify reviews into positive or negative sentiment. Alternatively, you can use the LightGBM model based on TF-IDF vectorized features.

3. Ranking Drugs
The script calculates composite scores for each drug and ranks them within each condition.

4. Visualizations
Generate visualizations such as:

Bar plots for the most common conditions and drugs.
Pie charts for distribution of conditions.
Word clouds for common words in high-rated and low-rated reviews.
5. Output
The top-ranked drugs for each condition are stored in a CSV file, and visualizations are saved as images.

Running the Project
Clone this repository:

bash
Copy code
git clone https://github.com/yourusername/drug-recommender-system.git
Navigate to the project directory:

bash
Copy code
cd drug-recommender-system
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Run the Jupyter notebook or Python script to train the models, perform EDA, and rank the drugs:

bash
Copy code
jupyter notebook or python main.py
Results
The LSTM model achieved a test accuracy of 82.42%.
The LightGBM model achieved an accuracy of 81.84% using TF-IDF features.
The top drugs for various conditions are listed based on their composite score.
License
