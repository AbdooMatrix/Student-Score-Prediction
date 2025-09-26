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

   git clone https://github.com/AbdooMatrix/Student-Score-Prediction.git
   
   cd Student-Score-Prediction


Download the dataset and place it in the project directory (e.g., `data/` folder).  
Launch the notebook:

   jupyter notebook Student_Score_Prediction.ipynb


---

## 🚀 Usage Workflow

- **Load & Preprocess Data:**  
  Handle missing values by imputing the most frequent value (mode) for categorical columns such as TeacherQuality, ParentalEducationLevel, and DistancefromHome. Remove duplicate records to avoid redundancy.  
  Identify and clip outliers in numeric features (HoursStudied, Attendance, PreviousScores, TutoringSessions) and target variable (ExamScore) using the Interquartile Range (IQR) method to reduce noise and improve model robustness.

- **Exploratory Data Analysis (EDA):**  
  Visualize distributions and correlations of features with ExamScore. Conduct univariate and bivariate analyses with histograms, boxplots, and correlation heatmaps to understand variable behavior and relationships.

- **Feature Engineering & Selection:**  
  Perform hypothesis testing (ANOVA, t-tests) to evaluate the statistical significance of categorical variables; find that Gender and SchoolType have no meaningful impact on exam outcomes and exclude them. One-hot encode the relevant categorical variables remaining after selection.

- **Model Training:**  
  Build multiple regression models including Linear Regression and Polynomial Regression (degree 2). Standardize numeric features to optimize model convergence and stability.

- **Model Evaluation:**  
  Use metrics such as R², Root Mean Squared Error (RMSE), and Mean Absolute Error (MAE) to assess performance on test data. Apply 5-fold cross-validation to verify model generalizability and reduce overfitting risk.

- **Interpretation:**  
  Analyze model coefficients and feature importance to determine key predictors influencing exam scores, focusing on study hours and attendance as dominant factors.

---

## 📊 Results & Insights

- **Key Predictors:**  
  Study hours and attendance emerged as the strongest determinants of exam performance, aligned with education research emphasizing consistent engagement and preparation.

- **Outlier Treatment:**  
  Clipping outliers in critical numeric features and the target variable using the IQR method helped stabilize model training and improved prediction accuracy by minimizing the influence of extreme values.

- **Hypothesis Testing Findings:**  
  Statistical tests revealed no significant relationship between exam scores and categorical features like Gender and SchoolType (p-value > 0.05), leading to their removal to simplify modeling without loss of information.

- **Model Performance:**  
  Linear Regression achieved a test set R² approximately 0.86, demonstrating robust predictive power with relatively low prediction errors. The Polynomial Regression (degree 2) model yielded similar results with R² around 0.85, indicating that the underlying relationship between features and exam score is predominantly linear.

- **Model Stability:**  
  Consistent cross-validation scores indicated that models generalize well across different data folds, confirming their reliability.

- **Future Directions:**  
  Enhancements could include experimenting with regularization techniques like Ridge or Lasso regression to mitigate multicollinearity, introducing interaction terms to capture combined effects of features, or exploring advanced nonlinear models such as Random Forests or Gradient Boosting to potentially improve accuracy and uncover complex patterns.



