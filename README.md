# NLP Assignment 2 — Text Preprocessing & Document-Term Matrix

## Overview

This project focuses on fundamental Natural Language Processing (NLP) techniques for preprocessing and structuring textual data.

The analysis uses stand-up comedy transcripts to demonstrate how raw text can be cleaned, tokenized, transformed into structured representations, and prepared for downstream machine learning and NLP tasks.

## Objectives

* Acquire and prepare transcript data
* Perform systematic text cleaning
* Tokenize textual data
* Remove English stop words
* Organize transcripts into a reusable corpus
* Construct a Document-Term Matrix (DTM)
* Explore `CountVectorizer` parameters
* Understand the effect of n-grams and document-frequency thresholds

## NLP Pipeline

The notebook follows this workflow:

```text
Raw Transcripts
      ↓
Lowercase Conversion
      ↓
Punctuation Removal
      ↓
Number Removal
      ↓
Stage-Direction / Newline Cleaning
      ↓
Tokenization
      ↓
Stop-Word Removal
      ↓
Clean Corpus
      ↓
Document-Term Matrix
      ↓
CountVectorizer Experiments
```

## Text Preprocessing

The transcripts are processed through multiple cleaning stages:

1. Convert text to lowercase
2. Remove punctuation
3. Remove numerical values
4. Remove parenthetical stage directions
5. Remove newline characters
6. Apply an additional regular-expression cleaning pass
7. Tokenize the text
8. Remove common English stop words

A second cleaning function further normalizes whitespace and removes remaining unwanted characters.

## Corpus Representation

The cleaned transcripts are organized into a pandas DataFrame representing the corpus.

Each row corresponds to a comedian and contains the associated cleaned transcript.

The corpus is persisted as a pickle file so that it can be reused in subsequent NLP analysis.

## Document-Term Matrix

A Document-Term Matrix represents:

* Rows → documents/comedian transcripts
* Columns → vocabulary terms
* Values → word-frequency counts

The DTM is generated using Scikit-learn's `CountVectorizer`.

This representation can serve as input for downstream NLP and machine-learning techniques such as:

* Topic modeling
* Clustering
* Classification
* Sentiment analysis
* Feature analysis

## CountVectorizer Experiments

The notebook investigates three important `CountVectorizer` parameters.

### `ngram_range`

Controls the size of contiguous word sequences extracted from the corpus.

For example:

```python
ngram_range=(1, 2)
```

extracts both:

* Unigrams — individual words
* Bigrams — two-word sequences

### `min_df`

Controls the minimum document frequency required for a term to be included.

It can be used to remove extremely rare terms that may provide little useful information.

### `max_df`

Controls the maximum document frequency allowed for a term.

It can be used to remove terms appearing in an unusually large proportion of documents.

## Project Structure

```text
NLP-Assignment-2/
│
├── Assignment_2_Solution.ipynb
├── Assignment 2.pdf
├── README.md
└── data/
    └── Generated NLP artifacts
```

## Technologies Used

* Python
* Pandas
* NumPy
* NLTK
* Scikit-learn
* Regular Expressions
* Jupyter Notebook
* Matplotlib

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/keshee03/NLP-Assignment-2.git
cd NLP-Assignment-2
```

### 2. Install dependencies

```bash
pip install pandas numpy nltk scikit-learn matplotlib requests beautifulsoup4
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Assignment_2_Solution.ipynb
```

Run the notebook cells sequentially.

## Key Learning Outcomes

This assignment demonstrates practical understanding of:

* Text preprocessing
* Regular expressions
* Tokenization
* Stop-word removal
* Corpus construction
* Bag-of-Words representation
* Document-Term Matrices
* N-gram feature extraction
* Feature-frequency filtering
* Basic NLP data engineering

## Academic Context

This repository contains coursework demonstrating the application of NLP preprocessing and feature-engineering techniques to real-world textual data.

## Author

**Keshee Jain**

B.Tech — Computer Engineering

Thapar Institute of Engineering & Technology
