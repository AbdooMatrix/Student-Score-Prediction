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

- Python 3.7+  
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

- Load & preprocess data (handle missing values by mode imputation, drop duplicates)  
- Perform exploratory analysis (distributions, correlations, plots)  
- Apply hypothesis testing for feature relevance and encode categorical features  
- Train regression models (linear and polynomial degree 2)  
- Evaluate models using R², RMSE, MAE on the test set and 5-fold cross-validation  
- Analyze which factors most influence predictions  

---

## 📊 Results & Findings

- Linear regression test set R² ≈ 0.86 with good RMSE and MAE  
- Polynomial regression (degree 2) test set R² ≈ 0.855, slightly worse than linear  
- Feature selection and outlier handling improved model accuracy  
- Cross-validation indicates stable model performance  

---

## 🤝 Contributing

Contributions & suggestions are welcome! Feel free to:  
- Open an issue  
- Submit a pull request  
- Suggest enhancements (e.g., new models, deployment pipelines)  

---

## 📬 Contact

Abdelrahman Mostafa  
Email: [abdomostafa20188@gmail.com](mailto:abdomostafa20188@gmail.com)  
GitHub: [AbdooMatrix/Student-Score-Prediction](https://github.com/AbdooMatrix/Student-Score-Prediction)
