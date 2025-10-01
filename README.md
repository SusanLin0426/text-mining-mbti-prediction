# text-mining-mbti-prediction

---

## Project Overview
- **Goal**: Predict MBTI personality types from text posts.
- **Datasets**:
  - PersonalityCafe forum (Kaggle)
  - Twitter MBTI dataset (Kaggle)
  - Reddit MBTI dataset (Zenodo)
- **Preprocessing**:
  - Remove URLs & short posts
  - Lemmatization
  - TF-IDF vectorization
  - Balanced sampling (3% of total data, ~63,498 posts)
- **Models Tested**:
  - Logistic Regression
  - Linear SVC
  - Decision Tree
  - KNN
  - Multinomial Naive Bayes
  - Random Forest
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1 Score

---

## Results
- **16-class MBTI prediction**:
  - Best accuracy: Logistic Regression (0.287)
  - F1 scores < 0.25 across models
  - Strong bias toward INTP predictions due to dataset imbalance
- **Binary (dimension-level) classification**:
  - Much higher accuracy (>0.5 for most)
  - Best for S/N and I/E splits
- **Visualization**:
  - Word clouds by MBTI type and by platform
  - Distribution plots of posts per MBTI, platform, and dimensions

---

## Environment
- Python 3.9+
- Required libraries:
  - `pandas`, `numpy`
  - `scikit-learn`
  - `nltk`
  - `matplotlib`, `seaborn`
  - `wordcloud`
