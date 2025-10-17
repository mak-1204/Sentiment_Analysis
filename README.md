Sentiment Analysis Python 🤗 [YouTube Tutorial]
Overview

This notebook demonstrates how to perform sentiment analysis in Python, focusing on comparing a lexicon-based method (VADER) versus transformer models (e.g. RoBERTa) using a real text dataset. 
Kaggle

It is tied to a YouTube tutorial (as implied by the title).

Dataset

The dataset used is from Amazon Fine Food Reviews (sourced via Kaggle). 
Kaggle
+1

Key Steps / Contents

Environment Setup & Library Imports

Import libraries like pandas, numpy, matplotlib, seaborn, nltk, transformers, etc. 
Kaggle

Download NLTK dependencies (e.g. vader_lexicon) if not present.

Data Loading & Exploratory Data Analysis (EDA)

Load the Amazon Reviews dataset

Use .info(), check missing values, visualize distribution of review ratings

Plot counts of reviews by star rating 
Kaggle

Text Preprocessing (with NLTK)

Tokenization

POS (part-of-speech) tagging

Stop word removal

Lemmatization

VADER (Valence Aware Dictionary and sEntiment Reasoner)

Create a SentimentIntensityAnalyzer object

Compute polarity scores (compound, positive, negative, neutral) on texts

Map those scores to sentiment categories

Visualize how VADER’s compound scores relate to star ratings or categories

Transformer Model (RoBERTa, via Hugging Face)

Use AutoTokenizer and AutoModelForSequenceClassification

Tokenize text, run inference, get logits / probabilities

Use softmax to convert to probabilities and derive sentiment labels

Comparison: VADER vs RoBERTa

Plot scatter / pairplots or correlation between scores from both methods

Analyze where they differ, strengths/weaknesses

Hugging Face Pipeline for Sentiment Analysis

Use transformers.pipeline("sentiment-analysis")

Show how much simpler using pipeline is (few lines of code)

Test sample texts

Conclusion & Insights

Observations about correlation between VADER & RoBERTa

Transformer (RoBERTa) usually gives stronger, more confident predictions

But no method is perfect — errors exist

Using pipeline is convenient but may trade off fine control

References & Acknowledgements

Cites relevant tutorials, datasets, and research used

Links to tutorial video and original Kaggle notebook 
