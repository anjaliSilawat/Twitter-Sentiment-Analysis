# **Twitter-Sentiment-Analysis**
Developed a sentiment analysis model to classify tweets into positive, negative, or neutral categories, providing insights into public opinion using Python and machine learning techniques.

## **Purpose**
The purpose of this project is to perform sentiment analysis on tweets extracted from the Twitter API. By analyzing the sentiment expressed in tweets, we can gain insights into public opinion on various topics, trends, and events. This type of analysis is valuable for businesses, marketers, and researchers to understand customer feedback, social trends, and sentiment-driven behavior.

## **Objective**
- **Predict Sentiment**: Predict whether a given tweet expresses a positive, negative, or neutral sentiment.
- **Data Analysis**: Explore and analyze the dataset to identify patterns and trends.
- **Model Building**: Build and evaluate a machine learning model to classify tweets into sentiment categories.

## **Benefits**
- **Insights into Public Opinion**: Helps organizations understand the general sentiment of their audience.
- **Improved Decision-Making**: Enables data-driven decisions based on public sentiment.
- **Enhanced Customer Engagement**: Allows businesses to respond to feedback and improve customer satisfaction.

## **Technologies Used**
- **Python**: The primary programming language used for data processing and machine learning.

- **Libraries**:
  - **Pandas**: For data manipulation and analysis.
  - **NumPy**: For numerical operations.
  - **Matplotlib** and **Seaborn**: For data visualization and plotting.
  - **Scikit-learn**: For machine learning models and preprocessing.
  - **NLTK**: For natural language processing tasks.
  - **WordCloud**: For visualizing word frequencies.
  - **Emoji**: For handling emojis in text data.

- **Data**:
  - **Sentiment140 Dataset**: A large dataset containing 1,600,000 tweets labeled with sentiment (positive, negative, neutral).

## **Process and Workflow**

1. **Data Loading**:
   - Download and load the dataset from Kaggle.
   - Inspect and clean the dataset, handling missing values and duplicates.

2. **Data Analysis**:
   - Explore the distribution of sentiment classes.
   - Analyze tweet lengths and their relationship with sentiment.
   - Visualize sentiment distributions and correlations.

3. **Text Preprocessing**:
   - Encode and remove emojis.
   - Clean text data by removing special characters and URLs.

4. **Feature Engineering**:
   - Convert text data into numerical features using `CountVectorizer`.
   - Scale features using `MaxAbsScaler` to handle sparse matrices.

5. **Model Building and Evaluation**:
   - Build a `Logistic Regression` model to classify tweet sentiments.
   - Evaluate the model using accuracy, confusion matrix, and classification report.

6. **Testing**:
   - Test the model with new tweets to predict their sentiment.


