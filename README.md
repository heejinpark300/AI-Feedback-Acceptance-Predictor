# AI Feedback Acceptance Predictor

### A Machine Learning Prototype for Predicting Responses to AI-Generated Feedback

**Project Type:** Machine Learning · Human–AI Interaction · Educational AI  
**Developer:** Heejin Park, Ph.D.  
**Date:** October 2026  
**Status:** Educational Prototype

## 1. Project Overview

This project explores the technical feasibility of predicting how English language learners might respond to AI-generated feedback.

The prototype classifies responses into three categories:

- **Accept:** Accept AI feedback without modification.
- **Edit:** Modify AI feedback before use.
- **Reject:** Decide not to use AI feedback.

The project focuses on implementing an end-to-end machine learning workflow rather than establishing empirically validated learner behavior patterns.

## 2. Dataset

The project uses **300 synthetically generated observations** for demonstration purposes.

| Variable | Description |
|---|---|
| `trust_score` | Trust in AI, ranging from 0 to 100 |
| `english_level` | English proficiency: Beginner, Intermediate, Advanced |
| `ai_experience` | Previous AI experience: Low, Moderate, High |
| `decision` | Accept (0), Edit (1), Reject (2) |

The dataset contains no real learner responses.

## 3. Machine Learning Models

Two classification algorithms were implemented and compared:

- Logistic Regression
- Random Forest

The dataset was divided into 80% training and 20% testing data using stratified sampling.

## 4. Model Performance

| Model | Test Accuracy | Macro F1-score |
|---|---:|---:|
| Logistic Regression | 35.00% | 0.2684 |
| Random Forest | 30.00% | 0.2978 |

Random Forest was selected for the interactive demonstration because it supports multiclass prediction and feature-importance analysis.

**Important:** The target labels were randomly generated. Consequently, the observed predictive performance should not be interpreted as evidence that AI trust, English proficiency, or AI experience predicts real learner feedback behavior.

## 5. Interactive Streamlit Application

The application provides three functions:

1. **Behavior Prediction:** Predicts Accept, Edit, or Reject based on user-selected inputs.
2. **Model Performance:** Compares classification accuracy and Macro F1-scores and displays a confusion matrix.
3. **Feature Importance:** Visualizes the feature importance values calculated by Random Forest.

## 6. Technologies Used

- Python
- pandas
- scikit-learn
- Streamlit
- Matplotlib
- Joblib
- Jupyter Notebook

## 7. Limitations and Future Research

This project demonstrates the development of a functional machine learning prototype using synthetic data.

Its predictions are not validated against observed learner behavior, and the model should not be used to evaluate individual students or make educational decisions.

Future research could investigate actual learner responses to AI feedback, including acceptance, modification, rejection, and verification behaviors.

---

**Author:** Heejin Park, Ph.D.  
**Research Interests:** AI in Education · Human–AI Interaction · Responsible AI · Educational Technology
