# 🩺 DiaDetect-ML: Diabetes Prediction (Bachelor's Thesis)

This repository contains the notebook and code developed for my Bachelor's Thesis project. The goal of the study is to analyze clinical data and train various Machine Learning models to predict the onset of diabetes in patients.

---

## 📊 The Dataset

The data used to train and test the models comes from a public dataset available on **Kaggle**: 
🔗 **[Diabetes Prediction Dataset](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset)** *(insert the exact link here if you used a different version)*.

The dataset consists of 100,000 records and combines demographic data, medical history, and clinical measurements. The main features include:
* **Demographic Data:** `gender`, `age`.
* **Medical History and Lifestyle:** `hypertension`, `heart_disease`, `smoking_history`.
* **Medical Measurements:** `bmi` (Body Mass Index), `HbA1c_level`, `blood_glucose_level`.
* **Target:** `diabetes` (Binary variable: 0 = Negative, 1 = Positive).

---

## 🛠️ Pipeline and Methodology

Inside the `Lavoro_Tesi.ipynb` notebook, I developed a complete Data Science pipeline covering the following stages:

1. **Exploratory Data Analysis (EDA) and Data Cleaning:**
   * Identifying and handling missing values.
   * Identifying and removing duplicate records.
   * Visualizing class distribution using `Matplotlib` and `Seaborn`.

2. **Data Preprocessing:**
   * Normalizing and scaling continuous data using `MinMaxScaler` and `RobustScaler`.
   * Encoding categorical variables using `OneHotEncoder`.

3. **Handling Class Imbalance:**
   As a typical medical detection case, the dataset is highly imbalanced. I experimented with various techniques from the `imbalanced-learn` library:
   * **Over-sampling:** RandomOverSampler, SMOTE, BorderlineSMOTE.
   * **Under-sampling:** RandomUnderSampler, EditedNearestNeighbours (ENN), TomekLinks.
   * **Hybrid Techniques:** SMOTETomek.

4. **Model Training:**
   The following classification algorithms were tested and evaluated:
   * Logistic Regression
   * K-Nearest Neighbors (KNN)
   * Support Vector Classifier (SVC)
   * Random Forest Classifier

---

## 📈 Results Evaluation

In the medical field, reducing **False Negatives** (classifying a sick patient as "healthy") is of utmost importance. In this project, model evaluation heavily prioritized Recall metrics and confusion matrix analysis. Performances were summarized and ranked specifically based on the percentages of false negatives generated, in order to identify the safest model from a clinical perspective.

---

## 💻 Tech Stack

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn
* **Balancing:** Imbalanced-Learn (imblearn)
* **Data Visualization:** Matplotlib, Seaborn

---

## 🚀 How to Run the Project

1. Clone the repository:
   ```bash
   git clone [https://github.com/YourUsername/YourDiabetesRepo.git](https://github.com/YourUsername/YourDiabetesRepo.git)
   
2. Install the required dependencies:
  ```bash
    pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn tabulate
  ```
3. Download the dataset from Kaggle and place it in the root folder of the project.
4. Launch the notebook via Jupyter:
  ```bash
  jupyter notebook Lavoro_Tesi.ipynb
