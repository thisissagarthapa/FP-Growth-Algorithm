# FP-Growth Algorithm for Frequent Itemset Mining

## Project Overview
This project uses the FP-Growth algorithm to mine frequent itemsets from an Amazon transaction dataset. The dataset contains attributes like product name, category, price, and shipping details. The objective is to discover patterns and frequent item combinations based on customer purchases.

## Dataset
The dataset (`amazon_transactions.csv`) contains the following columns:
- `Transaction ID`
- `Product Name`
- `Product Category`
- `Price`
- `Quantity`
- `Customer ID`
- `Payment Method`
- `Shipping Country`

## Project Workflow
1. **Data Preprocessing:**
   - The `Transaction ID` and `Purchase Date` columns are dropped as they are not needed for mining frequent patterns.
   - A list of transactions (`market`) is created where each row contains the product-related strings such as product name, category, and payment method.

2. **FP-Growth Algorithm:**
   - The FP-Growth algorithm is applied to find frequent itemsets.
   - The `mlxtend` library is used to implement the algorithm with parameters:
     - `min_support=0.05`: Minimum support for an itemset to be considered frequent.
     - `max_len=3`: Maximum length of an itemset.

3. **Result:**
   - The frequent itemsets are extracted and sorted by support.
   - Examples of frequent itemsets include combinations of payment methods, product categories, and countries.

## Dependencies
- `numpy`
- `pandas`
- `seaborn`
- `matplotlib`
- `mlxtend`
- `collections`

Install the required libraries using:
```bash
pip install numpy pandas seaborn matplotlib mlxtend
