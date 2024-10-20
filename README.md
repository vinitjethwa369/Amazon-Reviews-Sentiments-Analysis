# Amazon Alexa Review Sentiment Analysis

This project involves analyzing Amazon Alexa product reviews to classify feedback as positive or negative based on the text of the reviews. The project uses Natural Language Processing (NLP) techniques, visualizations, and Machine Learning models to process and classify the reviews.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Preprocessing and EDA](#preprocessing-and-eda)
- [Model Training](#model-training)
- [Results](#results)
- [Visualizations](#visualizations)
- [Usage](#usage)


## Overview
The main objective of this project is to classify Amazon Alexa reviews as positive or negative based on the provided feedback using NLP techniques and machine learning models. The analysis includes:
- Exploratory Data Analysis (EDA) on ratings and feedback.
- Data preprocessing (handling missing values, text cleaning, stemming).
- Feature extraction using CountVectorizer.
- Training models like Random Forest, Decision Tree, and XGBoost.
- Visualizing word clouds for positive and negative reviews.

## Dataset
**Source:** The dataset contains reviews of Amazon Alexa products.

**File:** `amazon_alexa.tsv`

**Columns:**
- `rating`: The rating given by the user (1-5).
- `date`: Date of the review.
- `variation`: Product variation.
- `verified_reviews`: Review text.
- `feedback`: 1 for positive feedback, 0 for negative feedback.


## Installation
Clone the repository:
```bash
git clone https://github.com/your-username/amazon-alexa-review-analysis.git
cd amazon-alexa-review-analysis
```

Install the required dependencies:

```
pip install -r requirements.txt
```

Download the nltk stopwords:

```
import nltk
nltk.download('stopwords')
```

# Preprocessing and EDA
- Handling missing values in the verified_reviews column.
- Adding a new column length to store the length of each review.
- Visualizing the distribution of ratings using bar and pie charts.
- Generating word clouds for positive and negative reviews.
- Cleaning and stemming text data, and building a corpus for feature extraction.
  
# Model Training
Feature Extraction: Using CountVectorizer to convert text data into numerical form.

Train/Test Split: Splitting data into training and testing sets (70/30 split).

# Models:

- Random Forest
- Decision Tree
- XGBoost
  
**Evaluation:**

- Accuracy Score
- Confusion Matrix
- Model Saving: Saving the trained models using  ```pickle``` for future use.

# Results
- Best Model: XGBoost achieved the highest accuracy on the test data.
- Confusion Matrix: Visualization of predictions vs. actual feedback.
- Word Clouds:
  Positive reviews include words like "love," "great," "awesome."
  Negative reviews include words like "horrible," "refund," "repair."
  
## Visualizations

| Visualization          | Description                                   |
|------------------------|-----------------------------------------------|
| Ratings Bar Chart      | Distribution of ratings across reviews.      |
| Feedback Pie Chart     | Proportion of positive and negative feedback.|
| WordCloud (Positive)   | Common words in positive reviews.            |
| WordCloud (Negative)   | Common words in negative reviews.            |


# Usage
**Training the Model:**
```
python src/train.py
```

Making Predictions:

```
python src/predict.py --input "I love using Alexa for my smart home setup!"
```
**Jupyter Notebook:*** For detailed analysis, you can view the ```analysis.ipynb ``` file in a Jupyter notebook.


