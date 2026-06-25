# 🏦 Global Banking Customer Analytics Dataset (EDA) Project

## 📌 Project Overview

This project performs an in-depth **Exploratory Data Analysis (EDA)** on the **Global Banking Customer Analytics Dataset**. The objective is to analyze customer demographics, financial behavior, account information, risk profiles, debt levels, credit scores, and banking activity to uncover meaningful insights.

The notebook follows a complete EDA workflow, including:

* 📥 Data loading
* 🧹 Data cleaning
* ⚙️ Data preprocessing
* 🔍 Missing value inspection
* ♻️ Duplicate checking
* 📦 Outlier detection
* 📊 Statistical analysis
* 👥 Customer profiling
* 💰 Financial analysis
* 📈 Data visualization

---

# 📂 Dataset Information

The dataset contains banking customer records and financial information used to analyze customer behavior and account performance.

### 📋 Key Features

| Column                       | Description                            |
| ---------------------------- | -------------------------------------- |
| 👤 Full Name                 | Customer's full name                   |
| 📒 Account Type              | Type of bank account                   |
| 🌍 Country                   | Customer's country                     |
| 🏙️ City                     | Customer's city                        |
| 🎂 Age                       | Customer age                           |
| 🚻 Gender                    | Customer gender                        |
| 💵 Balance (USD)             | Account balance                        |
| 💳 Debt (USD)                | Outstanding debt                       |
| 📈 Income Level (USD Annual) | Annual income                          |
| 📊 Credit Score              | Customer credit score                  |
| ⚠️ Risk Category             | Risk classification                    |
| ✅ KYC Status                 | Know Your Customer verification status |
| ✅ Account Status            | Current account status                 |
| 📅 Account Creation Date     | Date account was opened                |
| ⏳ Last Active Date           | Last activity date                     |

---

# 🛠️ Technologies Used

* 🐍 Python
* 🐼 Pandas
* 🔢 NumPy
* 📈 Matplotlib
* 🎨 Seaborn
* 📓 Jupyter Notebook

---

# 📁 Project Structure

```text
📂 Global-Banking-Customer-Analytics-Dataset-EDA/
│
├── 📑 EDA Report of Global Banking Customers.pdf
├── 📊 Global Banking Customer Analytics Dataset.csv
├── 📓 Global Banking Customer Analytics Dataset.ipynb
├── 📖 README.md
│
└── 📁 outputs/
    ├── 📈 charts
    └── 📊 visualizations
```

---

## ▶️ How to Run the Project

### 1️⃣ 💻 Open Git Bash

### 2️⃣ 📥 Clone the Repository

```bash
git clone https://github.com/jesh-rijal/Global-Banking-Customer-Analytics-Dataset-EDA.git
```

### 3️⃣ 📂 Move into the Project Folder

```bash
cd Global-Banking-Customer-Analytics-Dataset-EDA
```

### 4️⃣ 📝 Open the Project in VS Code

```bash
code .
```

### 5️⃣ 📦 Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn notebook
```

### 6️⃣ 🚀 Run the Jupyter Notebook

📓 Open the notebook file **`Global Banking Customer Analytics Dataset.ipynb`** and run all cells sequentially to reproduce the **Exploratory Data Analysis (EDA)**.

---

# 🔍 Notebook Walkthrough

## 📚 1. Importing Libraries

The notebook begins by importing the required Python libraries.

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

### 🎯 Purpose

* 🔢 NumPy → Numerical operations
* 🐼 Pandas → Data manipulation
* 📈 Matplotlib → Data visualization
* 🎨 Seaborn → Statistical visualization

---

## 🗃️📥 2. Loading the Dataset

```python
dataset = pd.read_csv('Global Banking Customer Analytics Dataset.csv')
```

The dataset is loaded into a Pandas DataFrame for further analysis.

---

## 👀 3. Initial Data Inspection

The following methods are used:

```python
dataset.head()
dataset.tail()
dataset.sample(4)
dataset.shape
dataset.columns
```

### 🎯 Purpose

* 👀 View first records
* 📄 View last records
* 🎲 View random records
* 📏 Check dataset dimensions
* 🏷️ Display column names

---

## 🧹 4. Data Cleaning

The notebook removes unnecessary columns:

```python
dataset = dataset.drop(columns=['Username', 'Fraud Flag'])
```

### 🎯 Purpose

* 🗑️ Remove irrelevant information
* ⚡ Improve analysis efficiency
* 📊 Focus on meaningful features

---

## 🔍 5. Missing Value Analysis

```python
dataset.isnull().sum()
```

Checks missing values across all columns.

---

## ♻️ 6. Duplicate Record Analysis

```python
dataset.duplicated().sum()
```

Detects duplicate records in the dataset.

---

## 🧹 7. Handling Missing Values

```python
dataset = dataset.dropna()
```

Rows containing missing values are removed to ensure data quality.

---

## 📋 8. Understanding Customer Attributes

The notebook explores unique values from:

```python
Full Name
Account Type
Country
City
Age
Gender
Risk Category
KYC Status
Account Status
```

### 🎯 Purpose

Understand customer demographics and account characteristics.

---

## 📦 9. Outlier Detection

A boxplot is created for:

```python
Balance (USD)
Debt (USD)
Income Level (USD Annual)
```

### 📊 Visualization

```python
sns.boxplot()
```

### 🎯 Purpose

Identify unusual financial values and detect potential outliers.

---

# 📊 Exploratory Analysis

## 📒 Most Common Account Type

Identifies the most frequently used account type among customers.

---

## 🌍 Customer Distribution by Country

Determines which countries contain the highest number of banking customers.

---

## 🏙️ Customer Distribution by City

Analyzes customer concentration across cities.

---

## 👥 Customer Demographics Analysis

The notebook evaluates:

* 🎂 Age distribution
* 🚻 Gender distribution
* 🌍 Geographic distribution

---

## 💰 Financial Analysis

The notebook identifies:

* 💵 Highest account balance
* 💸 Lowest account balance
* 💳 Highest debt
* 💲 Lowest debt
* 📈 Highest annual income
* 📉 Lowest annual income
* 📊 Highest credit score
* 📋 Lowest credit score

---

## ⚠️ Risk Analysis

The notebook evaluates customer risk levels using:

```python
dataset['Risk Category']
```

### Insight

Helps identify the distribution of customers across different risk categories.

---

## ✅ KYC Analysis

The notebook analyzes:

```python
dataset['KYC Status']
```

### Insight

Measures customer verification compliance.

---

## 📇🔍 Account Status Analysis

The notebook evaluates:

```python
dataset['Account Status']
```

### Insight

Provides visibility into active and inactive accounts.

---

# 📈 Visualizations Included

### 📦 Financial Outlier Boxplot

Displays outliers in:

* Balance
* Debt
* Income

---

### 🏆 Top 50 Customers by Balance

Visualizes customers with the highest account balances.

---

### 🏷️📊 Account Type Distribution

Bar chart showing customer distribution by account type.

---

### 🌍 Customer Distribution by Country

Visualizes customer counts across countries.

---

### 🎖️🗺️ Top Locations by Average Balance

Displays the top country-city combinations with the highest average account balances.

---

### ⚠️ Risk Category by Country

Shows how customer risk profiles vary across countries.

---

### 🚻 Gender Distribution

Pie chart illustrating the proportion of male and female customers.

---

### 💵 Total Balance by Gender

Compares total account balances between genders.

---

### 💳 Debt Distribution

Histogram showing the frequency distribution of customer debt.

---

### ⚠️ Risk Category Distribution

Displays the number of customers in each risk category.

---

### ✅ KYC Status Distribution

Pie chart showing the proportion of verified and unverified customers.

---

# 🎯 Key Objectives

This analysis helps answer questions such as:

* 🏦 Which account type is most popular?
* 🌍 Which countries have the most customers?
* 💵 Who holds the highest balances?
* 💳 How is debt distributed among customers?
* 📈 What is the income distribution?
* ⚠️ How are customers categorized by risk?
* ✅ What percentage of customers completed KYC verification?

---

# 📌 Future Improvements

Potential enhancements:

* 🤖 Customer segmentation models
* 📈 Predictive analytics
* 🔭 Customer churn prediction
* ⚠️ Fraud detection models
* 📊 Interactive dashboards using Plotly
* 🌐 Business intelligence dashboards

---

# 🤝 Contributing

We welcome contributions from everyone! Follow the steps below to contribute.

---

## 1️⃣ Fork the Repository
Click the **Fork** button at the top right of this repository.

---

## 2️⃣ Clone Your Fork

Replace `<your-username>` and `<repository-name>` with your GitHub details:

```bash
git clone https://github.com/your-username/repository-name.git
cd repository-name
````

---

## 3️⃣ Create a New Branch

Create a meaningful branch name based on your work:

```bash
git checkout -b feature-name
```

💡 Examples:

* `add-customer-segmentation`
* `add-churn-prediction-model`
* `add-fraud-detection-analysis`

---

## 4️⃣ Make Your Changes

Add your improvements or fixes to the project.

---

## 5️⃣ Commit Your Changes

```bash
git commit -m "Add a clear description of your changes"
```

---

## 6️⃣ Push to GitHub

```bash
git push origin feature-name
```

---

## 7️⃣ Open a Pull Request

Go to the original repository and click **“New Pull Request”**.

Explain:

* What you changed
* Why you changed it

---

## ✅ Guidelines

* Keep code clean and readable
* Follow existing project style
* Test your changes before submitting PR
* Use meaningful commit messages

---

Thank you for contributing! 🚀

---

# 👨‍💻 Author

```bash
Name: Jesh Rijal
GitHub: My GitHub Profile: https://github.com/jesh-rijal
```
---

# 📜 License

This project is open-source and available for educational and learning purposes.

---

# ⭐ If you like this project

Give it a ⭐ on GitHub!
