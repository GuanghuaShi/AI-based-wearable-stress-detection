# AI-based-wearable-stress-detection
AI-based wearable stress detection using WESAD physiological data and PulseSensor + LSM6DSOX signals.

AI-Based Wearable Stress Detection

Project Overview

This project investigates machine learning approaches for wearable stress detection using physiological and motion signals.

The project uses the WESAD dataset for model development and evaluates cross-device performance using independently collected data from a PulseSensor and an Adafruit LSM6DSOX accelerometer.

Objectives

Extract physiological and motion features from wearable signals.

Compare BVP-only, ACC-only, and combined BVP + ACC models.

Evaluate participant-independent performance using Leave-One-Subject-Out (LOSO) cross-validation.

Investigate cross-device model transfer using independently collected wearable recordings.

Datasets and Sensors

Training dataset: WESAD

Self-collected wearable signals:

PulseSensor: PPG

Adafruit LSM6DSOX: 3-axis acceleration

Recording conditions:

Resting

Mental arithmetic

Public speaking

Walking

Feature Extraction

BVP sampling rate: 64 Hz

ACC sampling rate: 32 Hz

Window duration: 10 seconds

Baseline label: 0

Stress label: 1

BVP and ACC features are extracted separately and combined to evaluate the contribution of each signal type.

Machine Learning Models

Three classifiers are investigated:

Random Forest (RF)

Support Vector Machine (SVM)

XGBoost (XGB)

Three feature configurations are evaluated:

BVP-only

ACC-only

BVP + ACC

This produces nine model configurations.

Evaluation

WESAD model performance is evaluated using Leave-One-Subject-Out cross-validation.

The evaluation includes:

Accuracy

Balanced accuracy

Precision

Recall

F1-score

Specificity

External testing investigates model predictions on independently collected sensor recordings. These predictions are exploratory and are not treated as ground-truth accuracy measurements.

Repository Structure

Wearable-Stress-Detection/
├── notebooks/
├── data/
├── models/
├── results/
├── README.md
└── .gitignore

Technologies

Python

NumPy

Pandas

SciPy

Scikit-learn

XGBoost

Joblib

Google Colab

Author

Guanghua Shi

Disclaimer

This project is an academic research project. Model predictions are experimental and are not intended for clinical diagnosis or medical decision-making.
