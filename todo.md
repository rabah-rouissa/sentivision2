# A. Missing Data Cleaning Steps

(from DPCourse2&3 and DPCourse4)

## 1. Missingness mechanism analysis

Required by DPCourse2&3: MCAR / MAR / MNAR explanation
You skipped this.

## 2. Outlier detection

Required by DPCourse4 (IQR / Z-score / Isolation Forest)
You never applied outlier detection to:

- text length
- numerical features

Even if text data, DPCourse4 still expects at least one method.

## 3. Handling inconsistent data

From DPCourse2&3: inconsistent formats, symbols, whitespace, etc.
Your cleaning removed punctuation but didn't explicitly check:

- extra whitespace patterns
- repeated characters
- unicode anomalies
- emojis (they remain in the raw text before cleaning)

# B. Missing Text Preprocessing Steps

(from DPCourse7 & DPCourse8 "Text Preprocessing")

You implemented only the first 2 steps (lowercasing & punctuation removal).
The following required steps are missing:

## 1. Stopword removal

Required (see DPCourse7&8 — stopwords list).
TF-IDF uses built-in stopwords, but you must still show:

```python
from nltk.corpus import stopwords
```

and a custom stopword list if needed.

## 2. Tokenization demonstration

DPCourse7&8 requires explicit demonstration of:

- word_tokenize() OR
- spaCy tokenizer

You never show tokenized samples.

## 3. Stemming or Lemmatization

Required by DPCourse7&8:

- PorterStemmer
- WordNetLemmatizer

You did not stem or lemmatize anything.

## 4. POS tagging (optional but expected)

DPCourse8 includes a full POS tagging section — you skipped it.

## 5. Text encoding alternatives

(Required by DPCourse7&8)

You only used TF-IDF, but the course also expects you to:

- show Bag-of-Words (CountVectorizer)
- mention or test Word2Vec/GloVe embeddings
- explain limitations of BoW vs TF-IDF

Even a small demo is enough.
You did not include these.

# C. Missing Feature Engineering Steps

(from DPCourse6 & 7)

## 1. Feature redundancy / correlation analysis

You didn't provide:

- correlation matrix for numeric features
- multicollinearity checks
- mutual information / chi-square feature selection

## 2. PCA or dimensionality reduction

The course requires PCA demo (DPCourse6&7).
But you didn't apply:

- PCA for numeric features
- SVD for TF-IDF

(Even a small demonstration is needed.)

# D. Missing Model-Related Items

(from DPCourse6 & 7 and Project Guidelines)

## 1. Hyperparameter tuning

Guidelines mention tuning.
You didn't run GridSearchCV or RandomizedSearchCV.

## 2. Cross-validation evaluation

Preferred: stratified k-fold.
You only used a single train/test split.

## 3. Handling class imbalance

Your dataset is heavily imbalanced (positive >> neutral/negative).
You didn't try:

- class weights
- oversampling
- undersampling
- SMOTE (for numeric features)

Required by DPCourse2&3 under "data imbalance".

## 4. Error analysis

Guidelines request detailed error inspection:

- Look at misclassified examples
- Show typical FP/FN samples
- Discuss model behavior

You didn't do that.

## 5. Explainability

DPCourse7 requires:

- coefficients for Logistic Regression
- SHAP or LIME demo

You didn't include any explainability.

# E. Missing Deployment / Pipeline Extras

## 1. Saving the model and preprocessing

Project Guidelines require saving your pipeline.

## 2. Inference function

You should create:

```python
predict_sentiment(review_text)
```

## 3. Reproducibility & environment

You didn't include:

- random seeds
- environment specs

