# CIE2-Spam-Detection-Logistic-Regression-AD2111-
# SMS Spam Detection using Logistic Regression

## CIE 2 – Activity 2 | Unit II: Classification & Logistic Regression

## Project Overview

This project implements a binary classification model to identify whether an SMS message is **Spam** or **Ham (Legitimate)** using Logistic Regression.

The SMS text messages are converted into numerical features using TF-IDF (Term Frequency–Inverse Document Frequency), and the model predicts the probability of a message being spam.

## Objectives

- Perform data inspection and preprocessing.
- Identify and remove duplicate records.
- Analyze the distribution of Spam and Ham messages.
- Convert text data into numerical features using TF-IDF.
- Train a Logistic Regression classifier.
- Evaluate model performance using classification metrics.
- Analyze the impact of different classification thresholds.
- Predict new SMS messages.

## Dataset

**Dataset:** SMS Spam Collection Dataset

**Source:** [Kaggle – SMS Spam Collection Dataset](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)

The dataset contains SMS messages labeled as:

| Label | Meaning | Encoded Value |
|---|---|---:|
| Ham | Legitimate message | 0 |
| Spam | Unwanted message | 1 |

### Dataset after preprocessing

- Total messages: 5,169
- Ham messages: 4,516
- Spam messages: 653
- Features: Message text
- Target: Message label

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Methodology

### 1. Data Inspection
Examined dataset shape, columns, data types, missing values, and duplicate records.

### 2. Data Cleaning
- Removed unnecessary columns.
- Renamed columns to `label` and `message`.
- Removed duplicate records.

### 3. Label Encoding
Encoded the target labels:

- Ham → 0
- Spam → 1

### 4. Exploratory Data Analysis
Analyzed class distribution using counts and visualizations.

### 5. Train-Test Split
Divided the dataset into:

- 80% Training data
- 20% Testing data

Stratified sampling was used to maintain class proportions.

### 6. TF-IDF Feature Extraction
Converted SMS messages into numerical feature vectors using `TfidfVectorizer` with a maximum of 5,000 features.

### 7. Model Training
Trained a Logistic Regression model using the TF-IDF transformed training data.

### 8. Model Evaluation
Evaluated the model using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix
- Classification Report

### 9. Threshold Analysis
Analyzed model performance at different classification thresholds:

- 0.3
- 0.5
- 0.7

### 10. Baseline Comparison
Compared the trained model with a majority-class baseline.

### 11. New Message Prediction
Tested the model on new SMS messages to classify them as Spam or Ham.

## Threshold Analysis Results

| Threshold | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| 0.3 | 97.29% | 94.02% | 83.97% | 88.71% |
| 0.5 | 96.62% | 98.98% | 74.05% | 84.72% |
| 0.7 | 93.81% | 98.55% | 51.91% | 68.00% |

A lower threshold improves Spam Recall but may increase false positives. A higher threshold improves Precision but may miss more spam messages.

## Sample Predictions

| SMS Message | Prediction | Spam Probability |
|---|---|---:|
| Congratulations! You have won a free prize. Call now! | Spam | 0.8889 |
| Hey, are we meeting today at 6 pm? | Ham | 0.0263 |

## Project Structure

```text
CIE2-Spam-Detection-Logistic-Regression/
│
├── CIE2_Activity2_Spam_Detection.ipynb
├── spam.csv
└── README.md
```

## Conclusion

The SMS Spam Detection model was implemented using Logistic Regression. Text messages were transformed into numerical features using TF-IDF, and the classifier was trained to distinguish Spam from Ham messages.

The model was evaluated using multiple performance metrics, threshold analysis, and baseline comparison. The results demonstrated the application of Logistic Regression to binary text classification and the importance of selecting an appropriate classification threshold.

## Author

**Anushtha Maroti Balapure**

AI & Data Science Engineering Student

GitHub: [complexiota](https://github.com/complexiota)

