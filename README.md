Phishing Email Detection Using ACDFW and Random Forest

Project Overview

This project implements a machine learning-based phishing email detection system using the **CEAS 2008 Phishing Email Dataset.

The proposed approach combines TF-IDF feature extraction with an Adaptive Context-Aware Dynamic Feature Weighting (ACDFW) mechanism and a Random Forest classifier to classify emails as phishing or legitimate.

Proposed Workflow

Email Dataset
     ↓
Data Cleaning
     ↓
Text Preprocessing
     ↓
TF-IDF Feature Extraction
     ↓
ACDFW Context-Aware Weighting
     ↓
Feature Combination
     ↓
Random Forest Classification
     ↓
Model Evaluation


Dataset

Dataset:CEAS 2008 Phishing Email Dataset

The dataset contains labelled email records used for binary classification:

`0` – Legitimate email
`1` – Phishing email

The final dataset used in this project contains 39,039 email records with the following main attributes:

* `sender`
* `subject`
* `body`
* `urls`
* `label`

Dataset Access

The original dataset is not included in this GitHub repository because of its file size. The dataset used for this project can be obtained from the original Kaggle source.


The dataset should be downloaded and placed in the appropriate local dataset directory before executing the notebook.

Implementation

The implementation was developed using Python in Google Colaboratory (Jupyter Notebook).

Main technologies and libraries:

* Python
* Pandas
* NumPy
* Scikit-learn
* NLTK
* SciPy
* Matplotlib
* Joblib

Feature Engineering

The email sender, subject, and body are combined into a single textual representation. The text is then cleaned and transformed using TF-IDF.

The TF-IDF vectorizer was configured with:

* Maximum features: 5,000
* N-gram range: Unigrams and Bigrams

An additional context-aware feature is generated using the proposed ACDFW approach. This feature considers phishing-related keywords and URL information.

The final feature representation contains:

5,001 features

Machine Learning Model

A Random Forest Classifier is used for the final phishing email classification.

Configuration:

* Number of trees: 100
* Training data: 80%
* Testing data: 20%
* Stratified train-test split
* Random state: 42

Project Purpose

The purpose of this project is to demonstrate the application of data structures, algorithms, machine learning, object-oriented programming, and computational complexity analysis to a real-world cybersecurity problem.

Academic Work

This repository contains implementation materials for the COM713 Advanced Data Structures and Algorithms assignment.

The project was developed and tested individually using the dataset and methodology described above.

Dasun_Jayaweera_COM713_Assignment-Task-2
