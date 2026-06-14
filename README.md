# 🎬 AI Content-Based Movie Recommender System

## Project Overview

Recommendation systems power some of the world's largest digital platforms including Netflix, YouTube, Spotify, and Amazon.

This project develops an AI-powered content-based movie recommendation engine capable of suggesting similar movies by analyzing movie metadata and textual information.

The project progressively explores multiple Natural Language Processing approaches ranging from traditional Bag-of-Words models to semantic embeddings using Word2Vec.

---

# Business Problem

Users often struggle to discover relevant content from massive movie catalogs.

The goal of this project is to build a recommendation engine that can:

* Suggest similar movies
* Improve content discovery
* Personalize user experience
* Demonstrate modern NLP techniques used in recommendation systems

---

# Dataset

Source:

TMDB 5000 Movie Dataset

Files Used:

* tmdb_5000_movies.csv
* tmdb_5000_credits.csv

Key Features:

* Movie Overview
* Genres
* Keywords
* Cast
* Crew
* Metadata Information

---

# Project Workflow

## 1. Business Understanding

Understanding recommendation systems and their role in modern digital platforms.

---

## 2. Data Cleaning

Performed:

* Dataset merging
* Missing value handling
* Feature selection
* Duplicate checks

Final Features:

* Movie ID
* Title
* Overview
* Genres
* Keywords
* Cast
* Crew

---

## 3. Feature Engineering

Complex JSON-like structures were transformed into meaningful NLP features.

Examples:

* Genre extraction
* Keyword extraction
* Top cast extraction
* Director extraction

---

## 4. NLP Preprocessing

Applied:

* Lowercasing
* Tokenization
* Stopword removal
* Stemming
* Text normalization

Final semantic representation:

Movie tags combining:

* Overview
* Genres
* Keywords
* Cast
* Director

---

## Feature Engineering Output

<p align="center">
  <img src="images/new_dataset_overview.PNG" width="800">
</p>

---

# Model 1 — Bag of Words

Technique:

CountVectorizer

Pipeline:

Text → Vocabulary → Frequency Matrix → Cosine Similarity

Advantages:

* Simple
* Fast
* Interpretable

Results:

<p align="center">
  <img src="images/bag_of_words_results.PNG" width="800">
</p>

---

# Model 2 — TF-IDF

Technique:

TF-IDF Vectorization

Advantages:

* Reduces influence of common words
* Highlights informative terms
* Better weighting strategy

Results:

<p align="center">
  <img src="images/tfidf_results.PNG" width="800">
</p>


---

# Model 3 — Word2Vec Embeddings

Technique:

Word2Vec Semantic Embeddings

Architecture:

* Vector Size = 100
* Window = 5
* Min Count = 2

Advantages:

* Captures semantic relationships
* Learns contextual meaning
* Moves beyond simple keyword matching

Results:

<p align="center">
  <img src="images/w_2_v_results.PNG" width="800">
</p>


---


### Bag of Words

Strong keyword matching and thematic similarity.

### TF-IDF

More refined content matching with reduced noise.

### Word2Vec

Introduced semantic understanding but produced less stable recommendations due to document-level averaging limitations.

---

# Key Findings

* Bag-of-Words produced highly relevant recommendations for Avatar.
* TF-IDF improved weighting and reduced common-word influence.
* Word2Vec captured semantic relationships but struggled with long-document averaging.
* Recommendation quality depends heavily on text representation.

---

# Skills Demonstrated

### NLP

* Text Cleaning
* Tokenization
* Stopword Removal
* Stemming

### Feature Engineering

* Metadata Extraction
* JSON Parsing
* Semantic Tag Construction

### Machine Learning

* Vectorization
* Similarity Modeling
* Recommendation Systems

### Advanced NLP

* Bag of Words
* TF-IDF
* Word2Vec Embeddings

---

# Future Improvements

Next planned versions:

* FastText
* Doc2Vec
* BERT Embeddings
* Sentence Transformers
* Hybrid Recommendation Systems
* LLM-Powered Recommendations

---

# Technologies Used

* Python
* Pandas
* NumPy
* NLTK
* Scikit-Learn
* Gensim
* Matplotlib
* Seaborn

---

# Author

Oualid GASMI

Aspiring Data Scientist | NLP Enthusiast | AI & Machine Learning Learner
