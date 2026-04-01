# Twitter Sentiment Analysis

This project focuses on sentiment classification of Twitter data using different text preprocessing techniques, feature extraction methods and machine learning models. The goal is to evaluate how different text representations and classifiers affect performance.

## Project Overview

Sentiment analysis is a key task in Natural Language Processing (NLP) used to determine whether a piece of text expresses a **positive**, **neutral** or **negative** sentiment.

In this project, we:

- Preprocess raw Twitter text data
- Apply different feature extraction techniques
- Train and evaluate multiple machine learning models
- Compare performance across experiments

## Data Preprocessing

The dataset undergoes several preprocessing steps to clean and normalize the text:

- **Data Cleaning** (removing special characters, noise, and unnecessary symbols)
- **Case Normalization** (lowercasing text)
- **Tokenization**
- **Stop Word Removal**
- **Lemmatization**

These steps help reduce noise and improve model performance.

In addition, the target labels are transformed into numerical format using **Label Encoding**, allowing machine learning models to process the sentiment classes.

## Feature Extraction

Two main text representation techniques are used:

### 1. N-gram Vectorization

- Captures sequences of words (unigrams, bigrams, trigrams)
- Preserves local contextual information

### 2. TF-IDF Vectorization

- Assigns weights based on word importance
- Reduces the impact of common words

## Experiments

Three experiments were conducted to evaluate performance:

### Experiment 1: N-gram + SVM (Baseline)

- Uses N-gram features with Support Vector Machine
- Serves as the baseline model

### Experiment 2: TF-IDF + SVM

- Replaces N-grams with TF-IDF representation
- Evaluates the impact of feature weighting

### Experiment 3: TF-IDF + Random Forest

- Uses TF-IDF with Random Forest classifier
- Explores performance of an ensemble model

## Results Summary

| Experiment | Model                  | Accuracy  | Weighted F1 |
| ---------- | ---------------------- | --------- | ----------- |
| Exp 1      | N-gram + SVM           | ~0.68     | ~0.67       |
| Exp 2      | TF-IDF + SVM           | ~0.69     | ~0.69       |
| Exp 3      | TF-IDF + Random Forest | **~0.70** | **~0.70**   |

### Key Findings

- TF-IDF outperforms N-gram representation
- Random Forest improves performance over SVM
- Negative sentiment is the most difficult to classify

---

## Visualization

The project includes:

- Confusion matrices for each experiment
- Performance comparison chart (Accuracy & F1-score)

---

## Conclusion

Among all experiments, **TF-IDF + Random Forest** achieved the best performance. This suggests that combining weighted text representation with an ensemble model provides a more effective approach for sentiment classification.

## Project Structure

Twitter-Sentiment-Analysis/
│── data/
│ └── LabeledText.csv
│── twitter_sentiment_analysis.ipynb
│── requirements.txt
│── README.md

## How to Run

1. Clone the repository:

   git clone https://github.com/LimDeWei/twitter-sentiment-analysis.git

   cd twitter-sentiment-analysis

2. Install dependencies:
   pip install -r requirements.txt

3. Open the notebook using Jupyter Notebook or VS Code

4. Run all the cells

## Technologies Used

- Python
- Scikit-learn
- Pandas
- Numpy
- Matplotlib
- Seaborn
- NLTK

## Author

**Lim De Wei**
Computer Science (Data Science & AI)
Github: https://github.com/LimDeWei
Linkedln: https://www.linkedin.com/in/lim-de-wei-22809923a/
