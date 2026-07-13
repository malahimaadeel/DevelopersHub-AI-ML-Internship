# AI/ML Engineering Internship - Task Submissions
**Company:** DevelopersHub Corporation  
**Intern:** Malahima Adeel  
**University:** Bahria University, Karachi Campus  
**Program:** BS Remote & Intelligent Systems  

---

## 📋 Overview
This repository contains task submissions for the DevelopersHub Corporation AI/ML Engineering Internship (Basic + Advanced tracks). Projects cover Data Visualization, Classification, Regression, NLP with Transfer Learning, End-to-End ML Pipelines, and LLM Prompt Engineering.

| Track | Task | Title | Type |
| :--- | :--- | :--- | :--- |
| Basic | Task 1 | Exploring and Visualizing the Iris Dataset | Data Analysis & Visualization |
| Basic | Task 3 | Heart Disease Prediction | Binary Classification |
| Basic | Task 6 | House Price Prediction | Regression |
| Advanced | Task 1 | News Topic Classifier Using BERT | NLP + Transfer Learning |
| Advanced | Task 2 | End-to-End ML Pipeline — Customer Churn | ML Pipeline + GridSearch |
| Advanced | Task 5 | Auto Tagging Support Tickets Using LLM | Prompt Engineering |

---

## Basic Tasks (folder: `basic-tasks/`)

### 🌸 Task 1: Iris Dataset Exploration
**Goal:** To load, explore, and visualize the Iris dataset to understand feature distributions.

- **Dataset:** 150 samples, 4 features (Sepal/Petal length & width), 3 species.
- **Key Visualizations:**
    - **Pair Plots:** To see relationships between all feature pairs.
    - **Box Plots:** To identify the spread and median of each feature per species.
    - **Violin Plots:** To visualize the density of the data.
- **Finding:** Petal length and width are the most reliable features for separating the "Setosa" species from others.

### 🏥 Task 3: Heart Disease Prediction
**Goal:** Predict the presence of heart disease based on clinical data.

- **Algorithm:** Logistic Regression.
- **Preprocessing:** Applied `StandardScaler` for normalization.
- **Performance:**
    - **Accuracy:** ~85%
    - **AUC Score:** ~0.90 (Excellent discrimination)
- **Finding:** **Chest Pain Type (cp)** and **Max Heart Rate (thalach)** are the most significant predictors of heart disease.

### 🏠 Task 6: House Price Prediction
**Goal:** Predict median house values in California.

- **Algorithm:** Linear Regression.
- **Data Cleaning:** Used the **IQR (Interquartile Range)** method to remove extreme outliers.
- **Performance:**
    - **R² Score:** ~0.60 (Explains 60% of price variation).
- **Finding:** **Median Income (MedInc)** is the single most powerful predictor of house prices. Location (Latitude/Longitude) also plays a critical role.

---

## Advanced Tasks (folder: `advanced-tasks/`)

### 📰 Task 1: News Topic Classifier Using BERT
**Goal:** Fine-tune the BERT transformer model to automatically classify news headlines into 4 categories.

- **Dataset:** AG News Dataset — 120,000 training samples, 7,600 test samples, 4 balanced categories.
- **Model:** bert-base-uncased fine-tuned for 3 epochs using Hugging Face Trainer API.
- **Key Visualizations:**
  - Category Distribution Bar Chart: to verify class balance
  - Confusion Matrix: to see per-class prediction accuracy
- **Performance:**
  - Accuracy: ~87%
  - F1 Score: ~85-87%
- **Deployment:** Interactive Gradio web app — type any headline and get instant prediction with confidence scores.
- **Finding:** Sports and Business are easiest to classify due to distinct vocabulary. Transfer learning is highly effective even with only 2000 training samples.

### 🔄 Task 2: End-to-End ML Pipeline (Customer Churn Prediction)
**Goal:** Build a complete, reusable, production-ready pipeline that predicts whether a telecom customer will leave.

- **Dataset:** Telco Customer Churn — 7,043 customer records, 21 features.
- **Pipeline Steps:** Missing value imputation → Feature scaling → One-Hot Encoding → Model training — all chained automatically.
- **Algorithms:** Logistic Regression and Random Forest Classifier.
- **Tuning:** GridSearchCV tested 8 combinations × 3-fold CV = 24 training runs.
- **Performance:**

| Model | Accuracy |
|---|---|
| Logistic Regression | 78.75% |
| Random Forest | 77.75% |
| Tuned Random Forest (Best) | 80.44% |

- **Export:** Full pipeline saved to `churn_pipeline.pkl` using joblib — ready for reuse without retraining.
- **Finding:** Contract type and tenure are the strongest predictors of customer churn.

### 🎫 Task 5: Auto Tagging Support Tickets Using LLM
**Goal:** Automatically assign the top 3 most relevant tags to customer support tickets using prompt engineering.

- **Dataset:** Custom dataset of 10 realistic support tickets with 10 tag categories.
- **Model:** Llama-3.1-8b-instant via Groq API (free).
- **Three Techniques Compared:**
  - **Zero-Shot:** No examples provided — AI tags directly from task description. Fastest but least accurate.
  - **Few-Shot:** 3 example tickets with correct tags shown first — AI learns format from examples. Significantly more accurate.
  - **Chain-of-Thought:** AI reasons step-by-step before giving final answer — most accurate method.
- **Finding:** Chain-of-Thought prompting gives the best accuracy. Prompt engineering alone — without any model training — can solve real business problems effectively.

---

## 🛠️ Tech Stack
- **Languages:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib, Transformers, Datasets, Gradio, Requests
- **APIs:** Groq API (Llama-3.1), Hugging Face
- **Tools:** Google Colab, GitHub, joblib