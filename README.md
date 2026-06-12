# Social Media Sentiment Analysis — ML + GenAI Pipeline

## Overview

This project is an end-to-end Natural Language Processing (NLP) pipeline that performs sentiment classification on social media posts using Machine Learning and Generative AI. The system analyzes text and predicts whether a post expresses a positive or negative sentiment while also generating human-readable explanations for each prediction using LLaMA 3.3 70B.

The project combines traditional Machine Learning techniques with modern Generative AI to create an explainable sentiment analysis system capable of processing large-scale social media data.

---

## Problem Statement

Millions of users express opinions, emotions, and feedback on social media platforms every day. Manually analyzing such a large volume of data is impossible.

This project automates sentiment detection and helps organizations, researchers, and businesses understand public opinion, customer feedback, and social trends at scale.

---

## Dataset Information

| Attribute | Value |
|------------|------------|
| Dataset | Sentiment140 |
| Source | Kaggle |
| Total Records | 1,600,000 Tweets |
| Positive Samples | 800,000 |
| Negative Samples | 800,000 |
| Missing Values | 0 |
| Duplicate Records | 0 |
| Training Data | 1,280,000 Tweets (80%) |
| Testing Data | 320,000 Tweets (20%) |

---

## Project Workflow

### 1. Data Collection & Loading

- Loaded Sentiment140 dataset from Kaggle
- Verified data quality
- Checked dataset structure, missing values, and duplicates

### 2. Data Preprocessing

- Converted emojis into textual representation
- Removed URLs, mentions, punctuation, and special characters
- Lowercased text
- Cleaned noisy social media content
- Prepared data for feature extraction

### 3. Feature Engineering

#### CountVectorizer
- Generated Bag-of-Words representation
- Created approximately 589,114 textual features

#### TF-IDF Vectorizer
- Applied TF-IDF weighting
- Used Unigrams + Bigrams (`ngram_range=(1,2)`)
- Limited vocabulary to 100,000 features

### 4. Feature Scaling

- Applied MaxAbsScaler for sparse matrix scaling

### 5. Machine Learning Models

Four models were trained and compared:

1. Logistic Regression + CountVectorizer
2. Logistic Regression + TF-IDF
3. Naive Bayes + CountVectorizer
4. Naive Bayes + TF-IDF

---

## Model Performance

| Model | Accuracy |
|---------|---------|
| Logistic Regression + CountVectorizer | 80.02% |
| **Logistic Regression + TF-IDF** | **82.00%** |
| Naive Bayes + CountVectorizer | 78.07% |
| Naive Bayes + TF-IDF | 77.63% |

### Best Performing Model

**Logistic Regression + TF-IDF**

**Accuracy: 82.00%**

---

## Classification Report

| Class | Precision | Recall | F1-Score |
|---------|---------|---------|---------|
| Negative | 0.83 | 0.81 | 0.82 |
| Positive | 0.81 | 0.83 | 0.82 |
| Overall Accuracy | - | - | 0.82 |

**Testing Samples:** 320,000 Tweets

---

## Visualizations

- Sentiment Distribution Analysis
- Correlation Heatmap
- Model Accuracy Comparison Chart
- ROC Curve Analysis
- Confusion Matrix
- Positive Word Cloud
- Negative Word Cloud
- Tweet Length Distribution
- Top 20 Positive Words
- Top 20 Negative Words

---

## Generative AI Integration

### LLM Used

- LLaMA 3.3 70B
- Groq API

### Features

#### Sentiment Explainability Agent

The ML model predicts sentiment and confidence score. LLaMA then explains:

- Why the sentiment was predicted
- Which words influenced the prediction
- Whether the prediction appears reasonable

#### Batch Insight Generation

The system analyzes 100 labeled posts and automatically identifies:

- Major positive themes
- Major negative themes
- Linguistic patterns
- Dataset-level insights
- Improvement recommendations

#### Interactive Sentiment Analyzer

Users can test custom social media posts and receive:

- Sentiment prediction
- Confidence score
- AI-generated explanation

---

## Key Findings

- TF-IDF outperformed CountVectorizer by approximately 2%
- Logistic Regression outperformed Naive Bayes by approximately 4%
- Tweet length showed almost no correlation with sentiment (-0.006)
- The dataset was perfectly balanced
- The model achieved consistent performance across both sentiment classes

---

## Tech Stack

### Programming Language
- Python

### Data Processing
- Pandas
- NumPy

### Machine Learning
- Scikit-learn
- Logistic Regression
- Multinomial Naive Bayes

### NLP
- NLTK
- CountVectorizer
- TF-IDF Vectorizer
- WordCloud

### Visualization
- Matplotlib
- Seaborn

### Generative AI
- Groq API
- LLaMA 3.3 70B

### Model Persistence
- Pickle

### Development Environment
- Google Colab

---

## Future Improvements

- Multi-class sentiment classification (Positive, Neutral, Negative)
- BERT / DistilBERT implementation
- Streamlit deployment
- Real-time social media monitoring dashboard
- RAG-based sentiment knowledge assistant

---

## Results Summary

- Dataset Size: 1.6 Million Tweets
- Best Accuracy: 82.00%
- Best Model: Logistic Regression + TF-IDF
- Testing Samples: 320,000
- Models Compared: 4
- Visualizations Created: 10+
- LLM Used: LLaMA 3.3 70B
- GenAI Features Added: 3

---

## Author

**Anjali Silawat**

B.Tech, IGDTUW  
Machine Learning | AI | Data Analytics | Software Development
