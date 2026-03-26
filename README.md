# AI/ML Engineering Internship - Task Submissions
**Company:** DevelopersHub Corporation  
**Intern:** Malahima Adeel  
**University:** Bahria University, Karachi Campus  
**Program:** BS Remote & Intelligent Systems  

---

## 📋 Overview
This repository contains the selected tasks for the DevelopersHub Corporation AI/ML Internship. The projects cover Data Visualization, Binary Classification, and Regression.

| Task | Title | Type |
| :--- | :--- | :--- |
| **Task 1** | Exploring and Visualizing the Iris Dataset | Data Analysis & Visualization |
| **Task 3** | Heart Disease Prediction | Binary Classification |
| **Task 6** | House Price Prediction | Regression |

---

## 🌸 Task 1: Iris Dataset Exploration
**Goal:** To load, explore, and visualize the Iris dataset to understand feature distributions.

- **Dataset:** 150 samples, 4 features (Sepal/Petal length & width), 3 species.
- **Key Visualizations:** - **Pair Plots:** To see relationships between all feature pairs.
    - **Box Plots:** To identify the spread and median of each feature per species.
    - **Violin Plots:** To visualize the density of the data.
- **Finding:** Petal length and width are the most reliable features for separating the "Setosa" species from others.

---

## 🏥 Task 3: Heart Disease Prediction
**Goal:** Predict the presence of heart disease based on clinical data.

- **Algorithm:** Logistic Regression.
- **Preprocessing:** Applied `StandardScaler` for normalization.
- **Performance:** - **Accuracy:** ~85%
    - **AUC Score:** ~0.90 (Excellent discrimination)
- **Finding:** **Chest Pain Type (cp)** and **Max Heart Rate (thalach)** are the most significant predictors of heart disease.

---

## 🏠 Task 6: House Price Prediction
**Goal:** Predict median house values in California.

- **Algorithm:** Linear Regression.
- **Data Cleaning:** Used the **IQR (Interquartile Range)** method to remove extreme outliers.
- **Performance:** - **R² Score:** ~0.60 (Explains 60% of price variation).
- **Finding:** **Median Income (MedInc)** is the single most powerful predictor of house prices. Location (Latitude/Longitude) also plays a critical role.

---

## 🛠️ Tech Stack
- **Languages:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib
- **Tools:** Google Colab, GitHub

---
