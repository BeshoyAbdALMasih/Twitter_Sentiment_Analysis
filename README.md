# Twitter Sentiment Analysis

A notebook-based Twitter sentiment analysis project using the Sentiment140 dataset.  
The project vectorizes tweets with **TF-IDF** and trains classic classifiers (`BernoulliNB`, `LogisticRegression`, `LinearSVC`) to predict tweet sentiment (positive / negative). This repository contains the notebook `Twitter_Sentiment_Analysis.ipynb` that walks through data download, preprocessing, feature extraction, model training, evaluation, and simple experimentation.

---

## Table of Contents

- [Project Overview](#project-overview)  
- [Dataset](#dataset)  
- [Setup & Installation](#setup--installation)  
- [Running the Notebook](#running-the-notebook)  
- [What the Notebook Does (High-level)](#what-the-notebook-does-high-level)  
- [Notes & Tips](#notes--tips)  
- [Extending & Improvements](#extending--improvements)  
- [Reproducibility](#reproducibility)  
- [Requirements](#requirements)  
- [License & Contact](#license--contact)

---

## Project Overview

This repository demonstrates a classical machine-learning approach to sentiment analysis on Twitter data:

- Download the Sentiment140 dataset (1.6M tweets).
- Basic preprocessing (lowercasing; optional cleaning).
- Convert text to TF-IDF vectors using `sklearn.feature_extraction.text.TfidfVectorizer`.
- Train and evaluate multiple classifiers: `BernoulliNB`, `LogisticRegression`, `LinearSVC`.
- Compare performance using accuracy and classification reports.

The work is notebook-first to make the pipeline easy to read and modify.
---

## Dataset

**Sentiment140** (a.k.a. `kazanova/sentiment140`) — ~1.6 million labeled tweets with polarity (0 = negative, 4 = positive).  
The notebook downloads the dataset using `kagglehub` by default (see notebook cell). You can also download manually via Kaggle CLI and update the path in the notebook.

Important: the dataset is large. Working with the full dataset requires sufficient RAM and time. Consider sampling for quick experiments.

---

## Setup & Installation

1. Clone the repository:
```bash
git clone https://github.com/BeshoyAbdALMasih/Twitter_Sentiment_Analysis.git
cd Twitter_Sentiment_Analysis
```
2. Create & activate a virtual environment (recommended):
```bash
python3 -m venv .venv
source .venv/bin/activate         # Linux / macOS
# .venv\Scripts\activate          # Windows (PowerShell: .venv\Scripts\Activate.ps1)
```
3. Install dependencies:
```bash
pip install -r requirements.txt
```
Running the Notebook
```bash
jupyter notebook Twitter_Sentiment_Analysis.ipynb
# or
jupyter lab Twitter_Sentiment_Analysis.ipynb
```
