# Fake News Detection using Machine Learning

## Project Overview
This project is designed to detect fake news using machine learning models. The dataset consists of two types of news articles: **real** and **fake**. The goal is to build multiple machine learning models that can classify news articles based on the textual content and predict whether a given article is real or fake. Various algorithms such as **Logistic Regression**, **Decision Tree Classifier**, **Random Forest Classifier**, and **Gradient Boosting Classifier** are used and compared for their performance.

## Dataset
The project uses two datasets that can be downloaded on [Kaggle](https://www.kaggle.com/code/therealsampat/fake-news-detection/input?select=True.csv)
:
- **True.csv**: Contains real news articles.
- **Fake.csv**: Contains fake news articles.

Each dataset includes text, subject, title, and date columns, which are processed to create a training set for the models.

## Project Workflow
1. **Data Preprocessing**:
   - Combine the two datasets (`True.csv` and `Fake.csv`).
   - Label the data: `1` for real news and `0` for fake news.
   - Clean the text by removing URLs, HTML tags, punctuation, digits, and converting all text to lowercase.
   - Drop unnecessary columns like `title`, `subject`, and `date`.

2. **Shuffling and Splitting**:
   - Shuffle the data to avoid any biases.
   - Split the dataset into training and testing sets using an 80/20 split.

3. **Feature Extraction**:
   - Convert the textual data into numerical features using the **TF-IDF Vectorizer**.

4. **Model Building**:
   - Train multiple models to predict the label (fake or real):
     - Logistic Regression
     - Decision Tree Classifier
     - Random Forest Classifier
     - Gradient Boosting Classifier

5. **Evaluation**:
   - Evaluate the models on test data using **accuracy score** and **classification reports** (Precision, Recall, F1-score).
   
6. **Manual Testing**:
   - A function allows manual input of a news article for prediction. It compares predictions from different classifiers (Logistic Regression, Decision Tree, Random Forest, Gradient Boosting).

## Results
The classification results are printed in the terminal, showing the performance metrics of each model. For a new article input, the system will output predictions from all four classifiers, indicating whether the news is **Fake** or **Real**.