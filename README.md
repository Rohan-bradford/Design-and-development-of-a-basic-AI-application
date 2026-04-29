🫀 Multimodal Heart Disease Diagnosis using AI
📌 Overview

This project explores the application of Artificial Intelligence (AI) for heart disease detection using multimodal data:

🧾 Tabular patient health records
🩻 Chest X-ray images

The goal is to build models that can:

Detect the presence of heart disease
Classify the severity level
Identify heart-related anomalies in X-rays
Improve image quality using generative models

⚠️ Note: This system is designed as a decision-support tool and does not replace medical expertise.

📂 Datasets
Dataset 1 — Tabular Data

Contains patient health records including:

Age, sex, cholesterol, blood pressure
Chest pain type, ECG results
Heart rate, exercise-induced angina
Vessel count, thalassemia, etc.

📌 Target:

level → Disease severity (0 = no disease, 1–4 = increasing severity)
Dataset 2 — X-ray Images

Chest radiographs categorized into 17 disease classes.

📌 Heart-related classes used:

Atherosclerosis of the aorta
Cardiomegaly
Pneumonia
Pneumosclerosis
Post-inflammatory changes
Post-traumatic rib deformation
🚀 Tasks
🔹 Task 1: Tabular Data Classification

Build models to predict heart disease:

Binary Classification
Output: Disease present / not present
Multi-class Classification
Output: Severity level (0–4)

📌 Techniques used:

Decision Trees
Random Forest
Naïve Bayes
Logistic Regression
SVM
Neural Networks

📌 Enhancements:

Feature selection
Normalisation / standardisation
🔹 Task 2: X-ray Image Classification

Develop a CNN-based model to classify:

Heart-related vs Non-heart-related diseases

📌 Input:

Raw images (no manual feature extraction)
🔹 Task 3: Image Denoising & Reconstruction

Use generative models to improve image quality:

Autoencoders / Variational Autoencoders (VAE)
(Optional) GANs

📌 Goal:

Reconstruct clean images from noisy inputs
Improve classification performance
⚙️ Methodology
Data preprocessing (cleaning, scaling, encoding)
Train/test split
Model training and comparison
Performance evaluation
Model integration into a usable system
📊 Evaluation Metrics
Classification Models
Accuracy
Precision
Recall
F1-score
Confusion Matrix
Image Reconstruction
RMSE (Root Mean Square Error)
Relative RMSE
🧠 System Implementation

A Python-based application that allows users to:

Input patient health data
Upload X-ray images
Receive predictions:
Disease presence
Severity level
Optionally apply image enhancement before classification
📈 Key Outcomes
Comparison of multiple AI models
Understanding feature importance in diagnosis
Insights into multimodal AI in healthcare
Evaluation of AI effectiveness in early disease detection
⚠️ Ethical Considerations
Patient data privacy and security
Risk of misuse of AI predictions
Importance of human medical supervision
Bias in datasets and model decisions
📄 Deliverables
📓 Jupyter Notebook (.ipynb)
📊 Evaluation results and visualisations
📝 Report (1000–1500 words)
🧩 Tech Stack
Python
Scikit-learn
TensorFlow / Keras
NumPy / Pandas
Matplotlib
💡 Future Improvements
Improve model accuracy with larger datasets
Use advanced deep learning architectures
Integrate real-time patient monitoring
Deploy as a web-based diagnostic tool
