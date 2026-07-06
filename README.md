# Predicting Heart Disease Risk with Machine Learning

## 👥 Team Information
**SAMAI TEAM**
* Simon CORBINUS - 37
* Gabin CLAVIER - 36
* Mathis BLANCHARD - 32

## 📝 Project Summary
The goal of this project is to predict if a patient is at risk of heart disease using Machine Learning algorithms. Early detection of cardiovascular diseases is crucial for proactive medical intervention. We analyzed clinical data, handled data preprocessing (including feature scaling and duplicate management), and trained three classification models (Logistic Regression, Random Forest, and K-Nearest Neighbors). In the medical field, we specifically prioritize the **Recall** metric to minimize false negatives, as failing to identify a sick patient carries severe risks.

## 📊 Dataset Description
* **Source:** Kaggle ("Heart Disease Dataset" by johnsmith88
* **URL:** https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset
* **Context:** The data dates from 1988 and consists of four databases (Cleveland, Hungary, Switzerland, and Long Beach V). 
* **Size:** Originally 1025 rows, reduced to **302 unique rows** after extensive data cleaning (removing 723 artificial duplicates). The dataset contains 14 columns.
* **Features:** Age, sex, chest pain type (cp), resting blood pressure (trestbps), serum cholesterol (chol), fasting blood sugar (fbs), resting ECG (restecg), maximum heart rate (thalach), exercise-induced angina (exang), ST depression (oldpeak), ST segment slope (slope), major vessels colored by fluoroscopy (ca), and thalassemia (thal).
* **Target Variable:** `target` (Binary: 1 = Heart Disease, 0 = No Heart Disease)
* **Limitations:** The Kaggle dataset was heavily oversampled. Identifying and dropping the duplicates was a critical preprocessing step to prevent data leakage and overfitting.

## ⚙️ How to Run the Notebook
1. Clone this repository to your local machine or open it in Google Colab.
2. Ensure you have the required dataset located at the root ( /heart.csv ).
3. Install the required Python libraries (see below).
4. Run the `project_notebook.ipynb` cell by cell from top to bottom.

## 📦 Required Libraries
To run the code, you will need the following environment / libraries installed (listed in `requirements.txt`):
* Python 3.x
* pandas
* numpy
* scikit-learn
* matplotlib
* seaborn

## 🏆 Main Results and Limitations
* **Best Model:** The **Random Forest** classifier achieved the best overall performance with an accuracy of **83.61%**, outperforming Logistic Regression (77.05%) and K-Nearest Neighbors (73.77%).
* **Medical Focus (Recall):** The Random Forest model achieved a **Recall of 90%** for detecting heart disease (Class 1). This indicates that the model successfully identifies 90% of sick patients, effectively minimizing dangerous false negatives.
* **Key Finding:** The Exploratory Data Analysis (EDA) revealed that chest pain type (`cp`) and maximum heart rate (`thalach`) are the strongest positive indicators of heart disease risk, while exercise-induced angina (`exang`) and the number of major vessels (`ca`) are strong negative indicators.
* **Responsible AI & Limitations:** This model is designed strictly as a *decision-support tool* and does not replace professional medical diagnosis. The sample size is relatively small (302 unique patients), and potential biases regarding demographic representation must be thoroughly evaluated before any clinical application.
