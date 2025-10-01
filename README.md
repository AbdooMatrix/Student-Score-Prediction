# Student Score Prediction 🎓

Predict students’ exam scores based on multiple academic & behavioral factors using regression modeling.

---

## 📌 Overview

This project investigates relationships between student features (study time, attendance, parental involvement, tutoring sessions, etc.) and final exam outcomes. It involves:

- Data cleaning, missing value imputation, and preprocessing  
- Exploratory Data Analysis (EDA)  
- Feature engineering (including hypothesis testing to select relevant features)  
- Regression modeling (linear and polynomial degree 2)  
- Model evaluation with cross-validation and metrics (R², RMSE, MAE)  

Some less impactful features, such as SleepHours and PhysicalActivity, were removed during feature selection.

---

## 🗂 Dataset

The dataset is the **Student Performance Factors** dataset (Kaggle).  
Key features include:

- Study hours  
- Attendance  
- Parental involvement  
- Previous exam/assignment scores  
- Tutoring sessions  
- Extracurricular activities  
- Sleep hours (removed in feature engineering)  
- And more  

---

## 🛠 Installation & Setup

### Requirements

- Python 
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  

Install dependencies with:

pip install pandas numpy matplotlib seaborn scikit-learn


### Setup

Clone this repo:

   ```bash
   git clone https://github.com/AbdooMatrix/Student-Score-Prediction.git
   cd student-score-prediction
   ```


Download the dataset and place it in the project directory (e.g., `data/` folder).  
Launch the notebook:

   jupyter notebook Student_Score_Prediction.ipynb


---

## 🚀 Usage Workflow

- Load the data, fill missing values with the most common category, and remove any duplicate rows.  
- Check the data by drawing charts and looking at numbers to understand which features affect the exam scores.  
- Use statistical tests to find which features matter most. Features like Gender and School Type did not affect scores, so they were removed.  
- Prepare the data by converting categories into numbers that models can understand.  
- Train two types of regression models: simple Linear Regression and Polynomial Regression (degree 2).  
- Measure how well the models work using R², RMSE, and MAE on test data. Use cross-validation to ensure models perform reliably on different data samples.  
- Look at which features have the biggest influence on the exam score predictions.

---

## 📊 Results & Insights

- Study hours and attendance are the strongest factors related to better exam results.  
- Outliers in key numeric features and exam scores were limited using a method called IQR to make models more stable.  
- Statistical tests found no meaningful effect of Gender and School Type on exam performance, so they were left out to keep the model simple.  
- Linear Regression gave a good R² of about 0.86, showing it predicts exam scores well.  
- Polynomial Regression had similar results with R² around 0.85, suggesting relationships are mostly linear.  
- Models were tested multiple times with cross-validation to confirm consistent performance.  
- Future steps could include using methods that reduce overfitting (like Ridge/Lasso), trying interactions between features, or testing more complex models such as Random Forests or Gradient Boosting.
