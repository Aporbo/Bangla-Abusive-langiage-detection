
# Bangla Abusive Language Detection - Version 1

## Overview

This project focuses on detecting abusive language in Bengali text using machine learning models. The initial implementation includes text preprocessing, feature extraction, class imbalance handling, and evaluation of multiple machine learning algorithms to classify text into one of four predefined categories.

## Dataset

The dataset used in this project consists of Bengali text labeled into the following classes:

- **Moderately Toxic**
- **Severely Toxic**
- **Threat**
- **Neutral**

### Data Cleaning

- Removed non-Bengali characters and irrelevant symbols using a custom cleaning function.
- Handled missing values by dropping rows with NaN values in the text column.
- Replaced numeric class labels with descriptive strings for better interpretability.

### Stopwords Removal

- Generated a list of stopwords by identifying commonly occurring words in the dataset.
- Removed these stopwords to improve feature quality.

### Encoding

- Encoded class labels using `LabelEncoder` to convert text labels into numerical format for model training.

## Feature Extraction

- Extracted unigram and bigram features using TF-IDF vectorization to represent the text data numerically.

## Handling Class Imbalance

- Used the SMOTE (Synthetic Minority Over-sampling Technique) algorithm to balance class distributions and prevent bias in model training.

## Model Training and Evaluation

### Models Used:

1. **Logistic Regression**
2. **Naive Bayes**
3. **K-Nearest Neighbors (KNN)**

### Results:

The models were evaluated on accuracy, precision, recall, and F1 score. Below are the performance metrics:

| Model               | Accuracy | Precision | Recall | F1 Score |
| ------------------- | -------- | --------- | ------ | -------- |
| Logistic Regression | 77.46%   | 77.70%    | 77.46% | 77.55%   |
| Naive Bayes         | 73.05%   | 72.23%    | 73.05% | 71.37%   |
| KNN                 | 54.57%   | 58.37%    | 54.57% | 45.79%   |

The best-performing model was **Logistic Regression**, which achieved the highest accuracy and balanced metrics across all evaluation parameters.

## Visualization

- Model performance metrics were visualized using bar charts.
- Confusion matrices were plotted to analyze the classification performance of each model.

## Predictions and Validation

- Implemented a function to display sample correct and incorrect predictions, along with their confidence scores.
- Class-wise accuracy was calculated to assess model performance for each category.

## Interactive User Input

- A feature was added to allow users to input Bengali sentences and receive predictions along with confidence scores.
- Example:
  - **Input:** “সাকিবের ক্ষমা নাইপাপনের মাংস খাই😹""
  - **Predicted Class:** **Severely Toxic**
  - **Confidence:** 41%

## Known Issues and Future Enhancements

### Version 1 Limitations:

1. **Limited Dataset:** Performance may be affected due to dataset diversity.
2. **Stopword List:** Stopwords were generated from the dataset itself, which may not generalize well.
3. **Feature Engineering:** Advanced techniques like word embeddings were not explored.

### Planned Enhancements for Version 2:

1. Incorporate more diverse dataset for better generalization.
2. Use advanced models such as transformer-based architectures (e.g., BERT).
3. Explore sentiment-aware and context-based features for improved predictions.
4. Optimize the preprocessing pipeline to handle edge cases more effectively.

## How to Use

1. Clone this repository and run the notebook file in Google Colab.
2. Upload your dataset when prompted.
3. Enter Bengali sentences for predictions and analysis.

---

This is **Version 1** of the Bangla Abusive Language Detection project.
