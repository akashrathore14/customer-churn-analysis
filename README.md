# 📉 Customer Churn Analysis (EDA)

An exploratory data analysis of **7,043 telecom customers** to understand why customers leave (churn) and which customer groups are most at risk. The project is built with Python (Pandas, NumPy, Matplotlib, Seaborn) and ends with practical recommendations to improve customer retention.

---

## 📌 Project Overview

Customer churn directly affects a telecom company's revenue. This analysis finds out **who is leaving, and why**, by comparing churned and retained customers across demographics, tenure, contract type, services used and payment method.

**Key question:** *Which customer groups have the highest churn, and what can the company do to retain them?*

---

## 📂 Repository Structure

```
├── Customer_Churn.csv                                    # Dataset (7,043 rows × 21 columns)
├── Customer_analysis_1.ipynb                             # Jupyter notebook with full analysis
├── Customer_Churn_Analysis_-_Overall_Conclusion.pdf      # Summary report of findings
└── README.md
```

---

## 🗃️ Dataset Description

The dataset (`Customer_Churn.csv`) has **7,043 customer records and 21 columns**.

| Column | Description |
|---|---|
| `customerID` | Unique customer ID |
| `gender` | Male / Female |
| `SeniorCitizen` | Whether the customer is a senior citizen (0 / 1) |
| `Partner`, `Dependents` | Whether the customer has a partner or dependents |
| `tenure` | Number of months the customer has stayed |
| `PhoneService`, `MultipleLines` | Phone service details |
| `InternetService` | DSL, Fiber optic or No |
| `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport` | Add-on services |
| `StreamingTV`, `StreamingMovies` | Streaming services |
| `Contract` | Month-to-month, One year or Two year |
| `PaperlessBilling` | Whether billing is paperless |
| `PaymentMethod` | Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic) |
| `MonthlyCharges`, `TotalCharges` | Monthly and total amount charged |
| `Churn` | Whether the customer left (Yes / No), the target column |

---

## 🧹 Data Preparation

- Replaced blank `TotalCharges` values with 0 (these customers have 0 tenure, so no charges were recorded) and converted the column to `float`
- Checked for missing values and duplicate customer IDs (none found)
- Converted `SeniorCitizen` from 0/1 to No/Yes for easier reading
- Reviewed data types and summary statistics with `df.info()` and `df.describe()`

---

## 🔎 Analysis Covered

- Overall churn rate (count and percentage)
- Churn by gender
- Churn by senior citizen status
- Churn by tenure
- Churn by contract type
- Churn by phone, internet and add-on services
- Churn by payment method

---

## 🔍 Key Findings

| Dimension | Result |
|---|---|
| **Overall churn** | 1,869 of 7,043 customers churned (**26.54%**) |
| **Gender** | No meaningful difference between male and female customers |
| **Senior citizens** | 41.7% churn vs 23.6% for non-seniors |
| **Tenure** | Churn is highest in the first 1–2 months; long-tenure customers stay |
| **Contract type** | Month-to-month 42.7% vs One year 11.3% vs Two year 2.8% |
| **Internet service** | Fiber optic 41.9% vs DSL 19.0% vs No internet 7.4% |
| **Add-on services** | Without Online Security: 41.8% vs 14.6% with it; without Tech Support: 41.6% vs 15.2% with it |
| **Payment method** | Electronic check 45.3% vs Mailed check 19.1%, Bank transfer 16.7%, Credit card 15.2% |

*Churn rates are calculated from the churned and retained customer counts in the notebook charts.*

---

## 💡 Business Recommendations

1. **Win customers in their first months** with onboarding calls, welcome offers and early check-ins.
2. **Move customers to longer contracts** by offering discounts or perks to month-to-month customers.
3. **Bundle Online Security and Tech Support** through free trials or discounted packages.
4. **Review Fiber optic service quality and pricing** to find the reasons behind its high churn.
5. **Encourage automatic payments** with incentives for customers paying by electronic check.
6. **Create a senior-friendly retention plan** with simpler plans and dedicated support.

---

## 🛠️ Tools & Libraries

- **Python 3**
- **Pandas** and **NumPy** for data manipulation
- **Matplotlib** and **Seaborn** for visualization
- **Jupyter Notebook**

---

## ▶️ How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/akashrathore14/customer-churn-analysis.git
   cd customer-churn-analysis
   ```
2. Install the required libraries
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Launch the notebook
   ```bash
   jupyter notebook Customer_analysis_1.ipynb
   ```
   Keep the CSV file in the same folder as the notebook, and make sure the file name in the notebook's `pd.read_csv(...)` line matches the CSV file name exactly.

---

## 👤 Author

**Akash Rathore**

---

⭐ If you found this project useful, consider giving it a star!
