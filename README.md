# ✈️ Flight Ticket Price Prediction 

## 📌 Project Context & Business Goal
Ticket prices for flights are highly dynamic and depend on a multitude of factors, such as the airline, the number of stops, the travel class, and the booking window. 

Working on behalf of a flight booking platform, the objective of this project is to understand the underlying drivers of flight prices, conduct a rigorous statistical analysis, and build a robust machine learning pipeline to predict ticket prices accurately. 

🎯 **Primary Business Objective:** Develop a predictive model that achieves a **Mean Absolute Error (MAE) of less than 15€**.

---

## 📊 Dataset Overview
The project utilizes a dataset (`Clean_Dataset.csv`) containing over **300,000 flight booking records**. 
* **Target Variable:** `price` (Note: The dataset prices are in INR, where the target MAE of < 15€ translates to roughly < 1350 INR).
* **Key Features:**
  * `airline`: The company operating the flight (e.g., Vistara, AirAsia, Indigo).
  * `stops`: Number of layovers (Zero, One, Two or more).
  * `class`: Travel class (Economy, Business).
  * `days_left`: Number of days between the booking date and the flight.
  * `duration`: Total duration of the flight.
  * `source_city` / `destination_city` / `departure_time` / `arrival_time`.

---

## 🧠 Project Workflow & Methodology

The project is divided into three distinct phases, documented across three Jupyter Notebooks:

### 1. Exploratory Data Analysis (EDA)
**File:** `Machine_Learning_Prediction_Prix_billet_avion.ipynb`
* **Univariate Analysis:** Explored the distribution of categorical variables (flights per airline, source/destination cities, stops, ticket class) and continuous variables (duration, price).
* **Multivariate Analysis:** Visualized the relationship between features and the target variable (e.g., Price vs. Airline, Price vs. Days Left).

### 2. Statistical Hypothesis Testing
**File:** `Test_Statistique_ML_Prediction_Prix_billet_avion.ipynb`
To validate our visual observations, we formulated and tested several statistical hypotheses (α = 0.05):
* **T-Test:** Confirmed a significant price difference between direct flights and flights with stops.
* **ANOVA:** Validated that the choice of airline significantly impacts the ticket price.
* **T-Test:** Confirmed that Business class is significantly more expensive than Economy.
* **Pearson Correlation:** Proved a significant relationship between `days_left` (booking window) and `price`, validating dynamic pricing strategies.
* **Chi-Square:** Demonstrated a dependency between the chosen travel class and the booking timeline.

### 3. Preprocessing & Machine Learning
**File:** `Preproc_Model_ML_Prediction_Prix_billet_avion.ipynb`
* **Preprocessing:** * Dropped irrelevant columns (`Unnamed: 0`, `flight`).
  * Ordinal Encoding for `stops` and `class`.
  * One-Hot Encoding (OHE) for nominal variables (`airline`, `source_city`, `departure_time`, `arrival_time`, `destination_city`).
  * Feature scaling using `StandardScaler` on continuous features (`duration`, `days_left`).
* **Modeling & Evaluation:**
  We trained and evaluated multiple models to benchmark performance:
  1. **Dummy Regressor (Baseline):** MAE = 19,768 | R² = 0.00
  2. **Linear Regression:** MAE = 4,500 | R² = 0.909
  3. **Ridge Regression:** MAE = 4,500 | R² = 0.909
  4. **Random Forest Regressor:** MAE = 1,082 | R² = 0.984

---

## 🏆 Final Results & Conclusion

The **Random Forest Regressor** outperformed all other models and was selected as the final model. 

* **Final MAE:** 1,082 INR (Approximately **~12€**)
* **RMSE:** 2,790 INR
* **R² Score:** 0.9849 (The model explains 98.5% of the variance in ticket prices).
* **95% Confidence Interval for MAE:** [1061.62 INR, 1102.77 INR]

**Business Goal Reached:** The final MAE is well below the 15€ threshold demanded by the business requirements. The model has been successfully exported as `random_forest_model.joblib` for future deployment.

---

## 🧰 Technologies & Libraries

* **Language:** Python 3
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Statistical Tests:** SciPy (`ttest_ind`, `f_oneway`, `pearsonr`, `chi2_contingency`)
* **Machine Learning:** Scikit-Learn
* **Model Serialization:** Joblib

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
```

---

---

## 👥 Team

- Nouhaila
- Youssef
- Abdelghani
- abdelilah

---






