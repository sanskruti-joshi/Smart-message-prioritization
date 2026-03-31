# Smart Message Prioritization

A machine learning-based system to automatically classify text messages into **Low, Medium, and High urgency levels**, enabling efficient message prioritization in modern communication systems.

---

## Overview

In today's digital environment, users receive a large volume of messages, many of which do not require immediate attention. This project addresses the need for **automated urgency detection** by classifying messages based on **time-sensitive cues and linguistic patterns**.

The system uses **multi-class classification** to provide more granular prioritization compared to traditional binary approaches.

---

## Objectives

- Classify messages into:
  - **Low urgency** (no time constraint)
  - **Medium urgency** (future action required)
  - **High urgency** (immediate or same-day action)
- Improve message prioritization using machine learning
- Provide interpretable predictions using feature analysis
- Deploy a prototype API for real-world usage

---

## Methodology

### 1. Data Preparation
- Manually curated dataset of short, informal messages
- Time-based annotation rules for consistent labeling

### 2. Preprocessing
- Lowercasing and cleaning text
- Removal of non-alphabetic characters
- Stopword filtering

### 3. Feature Engineering
- **TF–IDF (unigrams & bigrams)**
- Linguistic features:
  - Message length
  - Exclamation count
  - Capitalization ratio
  - Urgency keyword flag

### 4. Models Used
- Logistic Regression
- Decision Tree
- Random Forest

---

## Results

- Logistic Regression achieved the highest performance with strong macro F1-score
- High urgency messages were classified with near-perfect accuracy
- Minimal confusion observed between Medium and High urgency classes

---

## Explainability

- Feature importance analysis highlights:
  - Temporal keywords (e.g., "today", "now")
  - Stylistic cues (capitalization, punctuation)
- Provides interpretable insights into model decisions

---

## Deployment

- Implemented as a **FastAPI-based REST API**
- Accepts a message and returns:
  - Predicted urgency level
  - Confidence scores for each class
- Tested in a cloud-based notebook environment

---

## Tech Stack

- Python  
- Scikit-learn  
- Pandas, NumPy  
- FastAPI  
- Matplotlib / Seaborn  

---

## Limitations

- Does not consider conversational context
- Relies on explicit temporal expressions
- Dataset is manually curated

---

## Future Work

- Context-aware urgency detection
- Integration with messaging platforms
- Use of transformer-based models (e.g., BERT)
- Real-time deployment pipelines

---

## Conclusion

This project demonstrates that **lightweight, interpretable machine learning models** can effectively perform multi-level urgency detection and support smart message prioritization in real-world scenarios.

---

## Report

Full project report available in the `/docs` folder.
