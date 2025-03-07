# Sentiment Analysis of User Reviews

## Project Overview
This project performs sentiment analysis on spotify user reviews to classify them into three categories: "Good," "Neutral," and "Bad." The aim is to develop a machine learning model capable of accurately predicting sentiment based on text reviews. The project involves data preprocessing, visualization, handling data imbalance, and implementing three different classification models to determine the best-performing approach.

## Dataset
The dataset consists of user reviews and their corresponding ratings. Ratings range from 1 to 5 and are transformed into categorical sentiment labels.
## Methodology
### 1. Data Preprocessing
- Ratings were converted into categorical sentiment labels ranging between 1 and 5 i.e  Ratings 4 & 5 → "Good", Rating 3 → "Neutral" and Ratings 1 & 2 → "Bad".
- I limited the dataset to include only the first 30,000 reviews to avoid crashing.
- Text data was cleaned by converting it to lowercase, removing stop words, punctuation, and applying lemmatization using SpaCy.

### 2. Exploratory Data Analysis
- A word cloud object was created to visualize common words present in the reviews.
- A bar graph was also plotted to show the distribution of ratings and to also visualize the imbalance in the ratings column.

### 3. Feature Extraction
The textual data was then converted into numerical format using the TF-IDF vectorizer.

### 4. Handling Class Imbalance
SMOTE (Synthetic Minority Over-sampling Technique) was then applied on the dataset in order to handle the imbalance in the rating column and balance the classes.

### 5. Model Training and Evaluation
**a) Logistic Regression** - The model was trained and its performance was evaluated using classification report, f1-score, and confusion matrix.

**b) Support Vector Classification (SVM)** - The model was trained using a linear kernel and evaluated using classification report, f1-score, and confusion matrix.

**c) Random Forest Classifier** - The model was trained and its performance was also evaluated using classification report, f1-score, and confusion matrix.

### 6. Prediction on Sample Reviews
Predictions were made on example reviews using the best-performing model (Logistic Regression).
- Example results:
  - "This app is so great!" → Good
  - "My Spotify is always lagging. Horrible experience." → Bad
  - "Works just fine but the ads are annoying." → Neutral

## Key Insights
- Logistic Regression and SVM performed better with text data due to their ability to handle high-dimensional, sparse data.
- Random Forest tends to be biased towards the majority class when dealing with imbalanced data such as the one used, hence giving wrong results.

## Conclusion
This project demonstrates how machine learning models can be leveraged for sentiment analysis. By preprocessing text data, handling class imbalance, and using appropriate models, we can build an effective classifier to categorize user reviews into positive, neutral, or negative sentiments.


