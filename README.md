# Minor_project_2
📌 Project Overview

SpendDNA is a Python-based personal finance analytics project that analyzes transaction data to understand spending behaviour, identify spending patterns, detect unusual transactions, and classify the user's spending personality.

The project processes raw transaction data and converts it into meaningful financial insights using Python, Pandas, and NumPy.

🎯 Objectives
Clean and standardize transaction data
Extract canonical vendor names from transaction descriptions
Categorize transactions based on vendors
Calculate overall spending and savings
Analyze monthly spending trends
Identify time-of-day spending patterns
Detect unusual transactions using statistical analysis
Identify the user's spending archetype
🚀 Features
1. Transaction Parser

Cleans and standardizes the raw transaction dataset.

Parses multiple date formats
Converts different amount formats into numeric values
Standardizes debit and credit transaction types
Handles missing values
Removes duplicate transactions
Creates a cleaned transaction DataFrame
2. Vendor Extractor

Extracts a standardized vendor name from messy transaction descriptions.

Examples:

BUNDL → Swiggy
SWIGGY → Swiggy
AMAZON → Amazon
ZEPTO → Zepto

Also identifies:

P2P transfers
ATM withdrawals
Uncategorised transactions
3. Category Tagger

Maps vendors into meaningful spending categories.

Example categories:

Food Delivery
Quick Commerce
E-commerce
Transport
Cafe
Restaurants
Subscriptions
Utilities
Groceries
Investments
Fuel
Entertainment
Personal Transfer
Cash Withdrawal
4. Spending Overview

Generates important financial statistics:

Total credits
Total debits
Net savings
Savings rate
Transaction count
Top 5 spending categories
Top 5 vendors

Savings rate is calculated as:

Savings Rate = (Total Credits - Total Debits) / Total Credits × 100
5. Monthly Trend Analysis

Analyzes spending across months.

Produces:

Category × Month spending matrix
Monthly spending totals
Category growth
Category decline
Biggest growth category
Biggest decline category
6. Time-of-Day Patterns

Analyzes spending according to the transaction hour.

Includes:

Category × Hour spending matrix
Peak spending hour
Late-night Food Delivery analysis
Cafe morning spending analysis
Hourly spending summary
7. Anomaly Detection

Detects unusually large transactions using a category-wise z-score.

Formula:

z = (amount - category_mean) / category_standard_deviation

Transactions with:

z-score > 2

are considered anomalies.

8. Spending Archetype Detection

Classifies spending behaviour into:

Foodie
Shopper
Investor
Commuter
Balanced

The classification is based on the user's spending shares across major categories.

🛠️ Technologies Used
Python
Pandas
NumPy
Jupyter Notebook / Google Colab

No machine-learning model is required for the core project.

📂 Project Structure
SpendDNA/
│
├── README.md
├── SpendDNA.ipynb
│
├── data/
│   └── rahul_transactions.csv
│
└── output/
    └── analysis_results

If you are not uploading the dataset to GitHub, keep the data/ folder out of the repository and mention how users can provide the dataset locally.

📊 Dataset

The project uses a transaction dataset containing fields such as:

Date
Time
Description
Type
Amount
Mode

The raw data contains approximately 1,328 transactions, including duplicate records. After cleaning, the project expects approximately 1,310 transactions covering 6 months.

▶️ How to Run
1. Clone the repository
git clone YOUR_GITHUB_REPOSITORY_URL
2. Open the project

Open:

SpendDNA.ipynb

using Google Colab or Jupyter Notebook.

3. Upload the dataset

Upload:

rahul_transactions.csv.zip

The notebook extracts the CSV and processes the transactions.

4. Run the notebook

Run the features in this order:

Feature 1 → Transaction Parser
        ↓
Feature 2 → Vendor Extractor
        ↓
Feature 3 → Category Tagger
        ↓
Feature 4 → Spending Overview
        ↓
Feature 5 → Monthly Trend Analysis
        ↓
Feature 6 → Time-of-Day Patterns
        ↓
Feature 7 → Anomaly Detection
        ↓
Feature 8 → Spending Archetype Detection
📈 Expected Results

The project specification gives approximate checkpoints including:

Clean transactions : ~1,310
Months covered     : 6
Total credits      : ~₹5.1 lakh
Total debits       : ~₹8.2 lakh
Savings rate       : ~-62%

Food Delivery is expected to be one of the dominant spending categories.

🔍 Key Insights

SpendDNA helps answer questions such as:

Where does most of the money go?
Which vendors receive the most money?
Which categories are increasing over time?
When during the day does spending peak?
How much Food Delivery spending occurs late at night?
Which transactions are unusually large?
What type of spender is the user?
📌 Project Requirements

The implementation follows the project constraints:

Python
Pandas
NumPy
No regular expressions
No matplotlib/seaborn for the core feature implementation
No machine-learning models for the mandatory features
👩‍💻 Author

Ayesha S
BE — Data Science

⭐ Project

SpendDNA: Personal Finance Analytics

Turning transaction data into meaningful spending insights.
