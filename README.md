# 📰 News Article Classification

Politecnico di Torino – Data Science & Machine Learning Lab

---

## 🎯 Overview

This project builds a machine learning model to classify news articles into **7 categories** using textual features. It uses TF-IDF vectorization and LinearSVC classification.

**Evaluation Metric:** Macro F1-score (~0.72)

---

## 📊 Dataset

- **Training:** `datasets/development.csv` (~28.8 MB)
- **Testing:** `datasets/evaluation.csv` (~7.2 MB)
- **Classes:** 7 news categories

---

## 🔧 Technology Stack

- Python 3.x
- Jupyter Notebooks
- Scikit-learn
- Pandas & NumPy
- Joblib

---

## 🚀 Quick Start

### Installation
```bash
pip install pandas scikit-learn joblib
```

### Run Training
```bash
jupyter notebook src/final.ipynb
```

This will:
1. Load and preprocess data
2. Extract TF-IDF features
3. Train LinearSVC model
4. Save `src/final_model.joblib`
5. Generate `src/submission.csv`

---

## 📂 Project Structure

```
News-Article-Classification/
├── datasets/
│   ├── development.csv
│   ├── evaluation.csv
│   └── sample_submission.csv
├── src/
│   ├── exploration.ipynb
│   ├── final.ipynb
│   ├── final_model.joblib
│   └── submission.csv
└── README.md
```

---

## 🔬 Methodology

### Preprocessing
- Remove escape characters
- Normalize contractions
- Merge: `source + title + article`

### Feature Extraction
- TF-IDF with 12,000 features
- Bigrams (1,2)
- English stop words removed

### Classification
- **Model:** LinearSVC
- **C:** 0.2
- **Class Weight:** balanced
- **Max Iterations:** 1000

---

## 📈 Model Performance

| Model | F1-Score |
|-------|----------|
| **LinearSVC** | **0.72** ✅ |
| Logistic Regression | 0.68 |
| SGD | 0.65 |
| Naive Bayes | 0.62 |

---

## 📝 License

MIT License - Politecnico di Torino

---

**Author:** [@omerzkan](https://github.com/omerzkan)
