# 🎓 Student Score Prediction

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-yellow.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Machine%20Learning-orange.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green.svg)
![Seaborn](https://img.shields.io/badge/Seaborn-EDA-teal.svg)

Predict students’ **exam scores** using regression models based on academic and behavioral factors.

---

## 📌 Overview
This project explores the **Student Performance Factors** dataset and examines how different academic and behavioral features influence exam results.  

The main goals are:
- Clean and preprocess raw data  
- Explore correlations and visualize trends  
- Select the most impactful features using hypothesis testing  
- Train regression models (Linear & Polynomial)  
- Evaluate with R², RMSE, MAE and cross-validation  

---

## 📂 Dataset
The dataset comes from [Kaggle: Student Performance Factors](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors).  

**Features include:**
- Study hours  
- Attendance  
- Parental involvement  
- Tutoring sessions  
- Previous scores  
- Extracurricular activities  
- Sleep hours (dropped in feature selection)  
- More demographic/behavioral attributes  

**Target:** `Exam_Score` (numerical final exam score)

---

## 🔑 Project Workflow

1. **Data Preprocessing**
   - Handle missing values with most frequent imputation  
   - Remove duplicates & invalid entries  
   - Outlier handling via IQR method  

2. **Exploratory Data Analysis (EDA)**
   - Histograms, scatter plots, boxplots  
   - Correlation heatmap  
   - Statistical tests (ANOVA, t-tests)  

3. **Feature Engineering**
   - Dropped irrelevant features (Gender, School_Type)  
   - Encoded categorical features with `get_dummies`  
   - Normalized numerical features  

4. **Modeling**
   - Linear Regression  
   - Polynomial Regression (degree 2)  
   - Cross-validation for reliability  

5. **Evaluation**
   - Metrics: R², RMSE, MAE  
   - Visual comparison of predicted vs. actual exam scores  

---

## 📊 Results & Insights

- **Study Hours** and **Attendance** are the most predictive features.  
- **Gender** and **School Type** had no statistically significant effect.  
- **Linear Regression** achieved **R² ≈ 0.86** on the test set.  
- **Polynomial Regression** performed similarly (**R² ≈ 0.85**), confirming mostly linear relationships.  
- Future improvements: Ridge/Lasso regularization, feature interactions, or tree-based models (Random Forest, Gradient Boosting).  

---

## ▶️ How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/AbdooMatrix/Student-Score-Prediction.git
cd student-score-prediction
````

### 2. Create a Virtual Environment (recommended)

```bash
python -m venv venv
```

Activate it:

* **Windows**:

  ```bash
  venv\Scripts\activate
  ```

* **Mac/Linux**:

  ```bash
  source venv/bin/activate
  ```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Project

```bash
python main.py
```

This will:

* Load & preprocess the dataset
* Perform EDA
* Train Linear & Polynomial Regression models
* Print evaluation metrics
* Show visualizations (distributions, heatmaps, predicted vs actual scores)

### 5. (Optional) Run Jupyter Notebook

If you prefer an interactive exploration:

```bash
jupyter notebook
```

Then open `Student_Score_Prediction.ipynb` from your browser.
