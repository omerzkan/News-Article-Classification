# News Article Multi-Class Classification
Politecnico di Torino – Data Science & Machine Learning Lab

---

## Overview
This project builds a machine learning model to classify news articles into 7 categories using textual information (`source`, `title`, `article`).  
Evaluation metric: **Macro F1-score** (handles class imbalance).

---

## Method

### Preprocessing
- remove escape characters and extra spaces
- normalize contractions
- merge text columns:
```
all_text = source + title + article
```

### Feature Extraction
TF-IDF:
- max_features = 12000
- ngram_range = (1,2)
- stop_words = english
- sublinear_tf = True
- max_df = 0.7, min_df = 3

### Model
**LinearSVC**
- C = 0.2
- class_weight = balanced
- max_iter = 1000

---

## Validation
- Stratified 5-fold cross-validation
- Macro F1-score
- Compared models: LinearSVC, Logistic Regression, SGD, Naive Bayes  
- LinearSVC performed best (~0.72 Macro F1)

---

## Pipeline
```
Text → TF-IDF → LinearSVC
```

Implemented using `sklearn.Pipeline`.

---

## Usage

Install:
```bash
pip install pandas scikit-learn joblib
```

Run:
```
final.ipynb
```

This will:
1. train model
2. save `final_model.joblib`
3. generate predictions
4. create `submission.csv`

---

## Files
```
datasets/
src/final.ipynb
final_model.joblib
submission.csv
```

---