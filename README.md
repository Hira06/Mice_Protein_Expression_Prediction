# Mice Protein Expression Classification

This repository contains a machine learning project for **classifying mice samples** based on their protein expression profiles. The project was conducted as part of **CSE422 – Artificial Intelligence** at **BRAC University**.

## Project Overview

The goal of this project is to predict the class of mice samples (based on genotype, treatment, and behavior) using the expression levels of **77 proteins**. Protein expression profiling is important in biological research, for instance, in understanding diseases such as Down syndrome.

We applied multiple machine learning models and compared their performance to identify the most effective approach for this dataset.

## Dataset

- **Name:** Mice Protein Expression Data  
- **Samples:** 1,080 rows  
- **Features:** 82 (77 protein expressions + 5 categorical/ID columns)  
- **Target:** Class (8 unique combinations of genotype, treatment, and behavior)  
- **Type:** Multiclass classification  

### Preprocessing Steps

- Handled missing values (drop, mean, median imputation).  
- One-hot encoding for categorical features (Genotype, Treatment, Behavior).  
- Dropped unnecessary feature `MouseID`.  
- Standardized numerical features using `StandardScaler`.  
- Split dataset into 70% training and 30% testing using **stratified sampling**.

## Models Trained

- K-Nearest Neighbors (KNN)  
- Decision Tree  
- Logistic Regression  
- Neural Network (2 hidden layers, ReLU, dropout 30%, softmax output)

### Evaluation Metrics

- Accuracy  
- Precision  
- Recall  
- F1 Score  

**Summary of Test Set Performance:**

| Model | Accuracy | Precision | Recall | F1 Score |
|-------|---------|-----------|--------|----------|
| KNN | 0.978 | 0.978 | 0.978 | 0.978 |
| Decision Tree | 1.000 | 1.000 | 1.000 | 1.000 |
| Logistic Regression | 1.000 | 1.000 | 1.000 | 1.000 |
| Neural Network | 1.000 | 1.000 | 1.000 | 1.000 |

> ⚠ Note: Perfect performance suggests potential overfitting; cross-validation is recommended for generalization checks.

## How to Run

1. Open the notebook in **Google Colab**:  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/Mice_Protein_Expression_Prediction.ipynb)
2. Follow the cells to preprocess the data, train models, and evaluate performance.  
3. All required packages are listed at the top of the notebook.

## Key Insights

- Dataset is highly discriminative with clear class patterns.  
- Missing values and class imbalance were handled carefully.  
- Neural Network captured complex non-linear patterns, but overfitting may occur.  
- KNN provides robust performance with slightly lower risk of overfitting.  

## Authors

- **Israt Jahan Hira** (ID: 24241155, CSE, BRAC University)  
- **Nusrat Jahan Snigdha** (ID: 22101812, CSE, BRAC University)  

## Supervisors

- **Asif Hasan [AHC]**  
- **Asif Shahriar [SHAH]**

