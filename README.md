🪔 Diwali Sales — Exploratory Data Analysis
An end-to-end exploratory data analysis (EDA) of Diwali festive-season sales, uncovering how customer demographics, geography, and product preferences drive purchase behavior.
![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4c72b0)
![Plotly](https://img.shields.io/badge/Plotly-Interactive%20Charts-3f4f75)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
---
📌 Table of Contents
Project Overview
Project Structure
Dataset
Tech Stack
Methodology
Key Findings
Getting Started
Recommendations
---
🎯 Project Overview
The goal of this project is to analyze Diwali sales transactions to understand who buys, where they buy, and what they buy. The analysis covers data cleaning, univariate distributions, and bivariate/multivariate relationships between demographics (gender, age, marital status, occupation), geography (state, zone), and purchase behavior (orders, amount, product category).
---
📂 Project Structure
```
Diwali-Sales-EDA/
│
├── Dataset/
│   └── Diwali Sales Data.csv          # Raw sales data (11,251 rows)
│
├── Document/
│   └── Diwali_Sales_EDA_Documentation.pdf   # Full EDA report with charts & findings
│
├── Image/
│   └── ...                            # Exported charts and visuals
│
├── Notebook/
│   └── DIWALI_SALES_EDA.ipynb         # Jupyter notebook with complete analysis
│
└── README.md
```
Folder	Description
`Dataset/`	Source CSV file used for the analysis
`Document/`	Formal PDF report documenting the process and insights
`Image/`	Visualizations generated during the analysis
`Notebook/`	Jupyter notebook containing all code, from cleaning to visualization
---
📊 Dataset
Property	Value
File	`Diwali Sales Data.csv`
Rows	11,251
Columns	15 raw → 13 after cleaning
Key fields	Gender, Age, Marital_Status, State, Zone, Occupation, Product_Category, Orders, Amount
Raw column overview
Column	Type	Description
`User_ID`	int	Unique customer identifier
`Cust_name`	object	Customer name
`Product_ID`	object	Unique product identifier
`Gender`	object	M / F
`Age Group`	object	Age bracket
`Age`	int	Customer age
`Marital_Status`	int	0 = unmarried, 1 = married
`State`	object	Customer state
`Zone`	object	Geographic zone
`Occupation`	object	Customer occupation
`Product_Category`	object	Category of purchased product
`Orders`	int	Quantity ordered
`Amount`	float	Transaction value
`Status`, `unnamed1`	float	Empty columns (dropped)
---
🛠 Tech Stack
Language: Python 3
Data manipulation: Pandas
Visualization: Matplotlib, Seaborn, Plotly Express
Environment: Jupyter Notebook / Google Colab
---
🔬 Methodology
1. Data Cleaning
Dropped fully empty columns: `Status` and `unnamed1`
Checked for duplicates — 8 duplicate records identified
Imputed 12 missing values in `Amount` using the column median
Verified zero missing values across all columns post-cleaning
2. Univariate Analysis
Gender, marital status, zone, orders, age (histogram, KDE, boxplot, skewness), and amount (histogram, KDE, skewness).
3. Bivariate & Multivariate Analysis
Zone vs. Gender (cross-tabulation and normalized heatmap)
Top product categories by total sales
Transaction amount by zone and order quantity (grouped boxplot)
---
💡 Key Findings
👩 Female customers purchase substantially more than male customers.
💍 Unmarried customers account for a larger share of purchases than married customers.
📍 Central Zone leads in sales activity (~38% of transactions) for both genders, followed by Southern (~24%), Western (~17%), Northern (~13%), and Eastern (~7%).
🛒 Customers most commonly order 2 items per transaction.
🎂 Customers are young-to-middle-aged, concentrated around 25–35 years (age skewness: 1.18, right-skewed).
💰 Transaction amounts are moderately right-skewed (skewness: 0.56), typically between 5,000 and 10,000.
🍱 Food is the top category (~34M), more than double Clothing & Apparel (~16.5M) and Electronics & Gadgets (~15.6M).
📦 Median amounts are consistent across zones; Central shows the widest spread, Northern and Eastern show more high-value outliers, and Western is the most consistent.
---
🚀 Getting Started
Prerequisites
```bash
pip install pandas seaborn matplotlib plotly jupyter
```
Run the Analysis
Clone the repository
```bash
   git clone <your-repo-url>
   cd Diwali-Sales-EDA
   ```
Launch Jupyter
```bash
   jupyter notebook
   ```
Open `Notebook/DIWALI_SALES_EDA.ipynb`
Update the data path in the loading cell to point to the local dataset:
```python
   df = pd.read_csv("../Dataset/Diwali Sales Data.csv", encoding="unicode_escape")
   ```
Run all cells.
> **Note:** The notebook was originally built in Google Colab and reads from a Google Drive path. Update it as shown above when running locally.
---
📈 Recommendations
Target marketing toward women and the 25–35 age group, the core buying segment.
Prioritize Food, Apparel, and Electronics in inventory and festive promotions.
Strengthen presence in the Eastern and Northern zones, where share is lowest, and investigate their high-value outliers.
Bundle products in pairs, aligning with the most common order quantity.
---
📄 Documentation
The full report with all charts and commentary is available in `Document/Diwali_Sales_EDA_Documentation.pdf`.
---
👤 Author
Your Name
GitHub · LinkedIn
---
⭐ If you found this project useful, consider giving it a star!
