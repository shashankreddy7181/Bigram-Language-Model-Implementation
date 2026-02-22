# Bigram-Language-Model-Implementation     

This repository contains a Python implementation of a **Bigram Language Model** using Maximum Likelihood Estimation (MLE). The project demonstrates how to count word frequencies, calculate conditional probabilities, and evaluate the likelihood of specific sentences based on a provided corpus.

---
### NAME: SHASHANK REDDY DASARI    
### ID :700781569   

---

## 📖 Project Overview

The goal of this project is to build a simple statistical language model that predicts the probability of a word given the preceding word.

### Training Corpus

The model is trained on the following three sentences:

1. `<s> I love NLP </s>`
2. `<s> I love deep learning </s>`
3. `<s> deep learning is fun </s>`

---

## 🛠️ Features

* **Unigram & Bigram Counting:** Automatically extracts and counts individual tokens and adjacent word pairs.
* **MLE Probability Estimation:** Calculates probabilities using the formula:


* **Sentence Scoring:** A function to calculate the total probability of a sentence by multiplying the bigram probabilities of its components.
* **Model Comparison:** Compares two specific sentences to determine which one the model "prefers" (assigns a higher probability).

---

## 🚀 How It Works

### 1. Counting

The model scans the corpus to build two dictionaries:

* `unigram_counts`: Total occurrences of each word (e.g., `love`, `deep`).
* `bigram_counts`: Total occurrences of word pairs (e.g., `('I', 'love')`).

### 2. Probability Calculation

Using Maximum Likelihood Estimation, we determine the likelihood of a word following another. For example, if "I" appears 2 times and "I love" appears 2 times, the probability  is .

### 3. Evaluation

The model evaluates the following test sentences:

* **S1:** `<s> I love NLP </s>`
* **S2:** `<s> I love deep learning </s>`

---

## 📊 Results

Based on the implementation, the model generates the following scores:

| Sentence | Probability |
| --- | --- |
| **S1: I love NLP** | ~0.333 |
| **S2: I love deep learning** | ~0.167 |

**Conclusion:** The model prefers **S1** because it has a higher cumulative probability. This is primarily because S2 is longer; since each bigram probability is , adding more terms to the multiplication typically decreases the total probability.

---

