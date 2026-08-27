# NLP Assignment 3 — Exploratory Text Analysis

## Overview

This project focuses on Exploratory Data Analysis (EDA) of textual data using stand-up comedy transcripts.

Building upon the text preprocessing and structured representations developed in the previous assignment, this project explores word usage, vocabulary diversity, speaking rate, and relationships between different linguistic categories.

The goal is to identify patterns and differences across comedians through quantitative text analysis and visualization.

## Objectives

* Identify the most frequently used words
* Generate word clouds for transcript analysis
* Refine stop-word lists based on corpus-specific observations
* Measure vocabulary size for each comedian
* Calculate words spoken per minute
* Compare speaking rates across comedians
* Visualize relationships between different word categories
* Explore alternative linguistic measures beyond profanity counts

## Analysis Pipeline

```text
Processed Transcript Corpus
          ↓
    Word Frequency Analysis
          ↓
       Word Clouds
          ↓
   Stop-Word Refinement
          ↓
    Vocabulary Analysis
          ↓
  Words-Per-Minute Analysis
          ↓
 Category-Based Comparisons
          ↓
     Data Visualization
```

## 1. Most Common Words

The project identifies the most frequently occurring words in the transcripts.

The top 30 words are examined to identify terms that may have limited semantic value in the context of comedian-specific analysis.

These observations are then used to identify additional corpus-specific stop words.

## 2. Word Cloud Analysis

Word clouds are generated to provide a visual representation of word frequency.

A second word cloud is created after excluding additional corpus-specific stop words, allowing the analysis to focus on more meaningful vocabulary.

## 3. Vocabulary Size

Vocabulary diversity is investigated by calculating the number of unique words used by each comedian.

This provides a simple measure of lexical variety across the different transcripts.

A larger vocabulary does not necessarily indicate better content, but it provides a useful quantitative measure for comparing language usage between speakers.

## 4. Words Per Minute

The analysis estimates how quickly each comedian speaks by calculating words per minute (WPM).

The analysis uses the provided comedy-special runtimes:

```python id="1h4e0m"
run_times = [60, 59, 80, 60, 67, 73, 77, 63, 62, 58, 76, 79]
```

The resulting WPM values are visualized to identify comedians with comparatively faster and slower speaking rates.

## 5. Category-Based Text Analysis

The project compares different categories of words appearing in the comedy scripts.

Scatter plots are used to investigate relationships between word-count features across comedians.

Rather than relying exclusively on profanity counts, the analysis considers alternative linguistic categories that can provide additional context about comedian-specific language usage.

## Visualizations

The notebook uses visualizations to make patterns in the transcript data easier to interpret, including:

* Word-frequency visualizations
* Word clouds
* Vocabulary comparisons
* Words-per-minute comparisons
* Category-based scatter plots

## Dataset

The analysis is performed on a collection of stand-up comedy transcripts.

Each transcript represents the script of an individual comedian's comedy special.

The analysis treats each transcript as a document and compares linguistic characteristics across documents.

## Technologies Used

* Python
* Pandas
* NumPy
* NLTK
* Scikit-learn
* Matplotlib
* WordCloud
* Regular Expressions
* Jupyter Notebook

## How to Run

### 1. Clone the repository

```bash id="1c8o2u"
git clone https://github.com/keshee03/NLP-Assignment-3.git
cd NLP-Assignment-3
```

### 2. Install dependencies

```bash id="x3m8ai"
pip install pandas numpy nltk scikit-learn matplotlib wordcloud
```

### 3. Launch Jupyter Notebook

```bash id="t0e7zq"
jupyter notebook
```

Open:

```text id="0p8z2h"
Assignment_3_Solution.ipynb
```

Run the notebook cells sequentially.

## Key Learning Outcomes

This project demonstrates practical understanding of:

* Exploratory Text Analysis
* Word-frequency analysis
* Word clouds
* Corpus-specific stop-word refinement
* Vocabulary diversity
* Lexical analysis
* Words-per-minute analysis
* Feature comparison
* Scatter-plot visualization
* Interpreting patterns in textual data

## Relationship to Assignment 2

Assignment 3 extends the NLP workflow established in Assignment 2.

Assignment 2 focuses primarily on:

* Text cleaning
* Tokenization
* Stop-word removal
* Corpus construction
* Document-Term Matrix creation
* CountVectorizer experimentation

Assignment 3 uses the processed textual data for higher-level exploratory analysis and visualization.

## Academic Context

This repository contains coursework demonstrating exploratory analysis of textual data and the application of NLP techniques to compare linguistic patterns across documents.

## Author

**Keshee Jain**

B.Tech — Computer Engineering

Thapar Institute of Engineering & Technology

