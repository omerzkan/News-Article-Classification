# News Article Classification

## Overview

This project aims to classify news articles into predefined categories using machine learning techniques. It leverages natural language processing (NLP) methodologies and recent advancements in model architectures to deliver robust and efficient classification solutions.

## Methodology

1. **Data Collection**: Gathered a comprehensive dataset of news articles from various sources.
2. **Preprocessing**: Cleaned and preprocessed the text data, which includes tokenization, removing stop words, and normalization.
3. **Feature Extraction**: Utilized techniques like TF-IDF and word embeddings to convert text data into numerical vectors suitable for machine learning models.
4. **Model Training and Evaluation**: Tested various models including Logistic Regression, Random Forest, and Deep Learning architectures. Evaluated their performance using accuracy, precision, recall, and F1-score.
5. **Deployment**: Implemented the best-performing model using Flask to create a web API for real-time predictions.

## Model Performance

| Model                | Accuracy | Precision | Recall | F1-score |
|----------------------|----------|-----------|--------|----------|
| Logistic Regression   | 85%      | 84%       | 86%    | 85%      |
| Random Forest        | 87%      | 86%       | 88%    | 87%      |
| Deep Learning (LSTM) | 90%      | 89%       | 91%    | 90%      |

The Deep Learning model showed the best performance across all metrics and is recommended for production use.

## Installation Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/omerzkan/News-Article-Classification.git
   cd News-Article-Classification
   ```  
2. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```
3. Start the application:
   ```bash
   python app.py
   ```
4. Access the web API at `http://localhost:5000/`.

## Project Structure

```
News-Article-Classification/
│
├── app.py                 # Flask application for the web API
├── requirements.txt        # Python dependencies
├── models/                 # Directory containing trained models
├── data/                   # Dataset used for training
├── notebooks/              # Jupyter notebooks for exploratory data analysis
└── README.md               # Project documentation
```
