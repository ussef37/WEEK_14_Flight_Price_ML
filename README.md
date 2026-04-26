# ✈️ Flight Price Prediction Project

## 📌 Project Overview

Airline ticket prices fluctuate based on multiple factors such as flight duration, booking timing, airline company, and number of stops.

This project aims to:
- Understand the key drivers of flight prices
- Perform a rigorous exploratory data analysis (EDA)
- Build a reliable machine learning model to predict ticket prices

🎯 **Business Goal:** Achieve a **Mean Absolute Error (MAE) < 15€** with a confidence interval.

---

## 📊 Dataset

- Source: `Clean_Dataset.csv`
- Size: **300,000+ flight records**
- Contains features such as:
  - Airline
  - Source & Destination
  - Duration
  - Number of stops
  - Days left before departure
  - Price (target variable)

---

## 🧠 Project Workflow

### 1️⃣ Data Loading
- Import required libraries
- Load dataset using Pandas
- Inspect structure and data types

---

### 2️⃣ Feature Understanding
- Identify:
  - Numerical vs Categorical variables
  - Discrete vs Continuous features
- Detect necessary transformations

---

### 3️⃣ Univariate Analysis
- **Categorical variables:**
  - Value counts
  - Bar plots

- **Numerical variables:**
  - Descriptive statistics
  - Histograms & Boxplots

---

### 4️⃣ Multivariate Analysis
Study relationships with target variable (Price):

- Duration vs Price
- Airline vs Price
- Stops vs Price
- Days left vs Price

📊 Tools used:
- Boxplots
- Grouped analysis
- Binning strategies

---

### 5️⃣ Statistical Hypothesis Testing

- Formulate hypotheses (H0 / H1)
- Apply statistical tests:
  - Pearson Correlation
  - ANOVA

📌 Significance level: **α = 0.05**

---

### 6️⃣ Data Preprocessing

- Handle missing values
- Encode categorical variables
- Transform ordinal features
- Scale numerical variables

✅ Build a **Scikit-learn Pipeline** to avoid data leakage

---

### 7️⃣ Modeling

Models tested:
- Dummy Regressor (Baseline)
- Linear Regression
- Ridge Regression
- Random Forest Regressor

📈 Evaluation metrics:
- MAE
- RMSE
- R² Score

📌 Use cross-validation for robust comparison

---

### 8️⃣ Final Evaluation

- Select best-performing model
- Train on full training dataset
- Evaluate on test set

---

### 9️⃣ Confidence Interval

- Compute absolute errors
- Estimate MAE
- Calculate standard error
- Build **95% confidence interval**

---

### 🔟 Model Export

- Save full pipeline (preprocessing + model)
- Format: `.joblib`
- Store model metadata

---

## 🧰 Technologies Used

- Python 🐍
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn

---

## 📁 Project Structure

WEEK_14_Flight_Price_ML/
├── Clean_Dataset.csv
├── Machine_Learning_Prediction_Prix_billet.ipynb
├── Preproc_Model_ML_Prediction_Prix_billet.ipynb
├── Test_Statistique_ML_Prediction_Prix_billet.ipynb
└── README.md

---

## 📈 Results

- ✅ Best Model: *(Random forest)*
- ✅ MAE: *(1082) = 11.48$*
- ✅ RMSE: *(2790)*
- ✅ R² Score: *(0.98)*

---

## 🎤 Presentation

The project includes:
- 📊 Data analysis insights
- 🤖 Model comparison
- 📌 Business interpretation

---

## 👥 Team

- Nouhaila
- Youssef
- Abdelghani
- abdelilah

---

## 🚀 How to Run

```bash
# Clone the repository
git clone <https://github.com/ussef37/WEEK_14_Flight_Price_ML.git>

# Navigate to project folder
cd flight-price-prediction

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter notebook