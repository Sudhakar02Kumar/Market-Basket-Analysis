# Market Basket Analysis Using Apriori Algorithm

## **Introduction**
Market Basket Analysis (MBA) is a data mining technique used to find associations or patterns in transaction data. It helps retailers and businesses to understand customer buying behavior and to discover relationships between products. This project applies the Apriori algorithm to identify frequent itemsets and generate association rules based on simulated transactional data.

The Apriori algorithm is a classical algorithm used for frequent itemset mining and association rule learning. It works by finding frequent itemsets in a database and then generating rules based on these frequent itemsets. The key metrics for evaluating the rules are support, confidence, and lift.

## **Methodology**

1. **Data Collection and Preparation:**
   - The dataset used in this project contains information about products categorized into different aisles.
   - The dataset is uploaded from a CSV file using `google.colab.files.upload()`.

2. **Data Processing:**
   - The relevant `aisle` column from the dataset is extracted into a list of aisles.
   - A set of simulated transactions (100 transactions) is generated, where each transaction is randomly chosen to contain between 1 and 5 aisles.

3. **Encoding Transactions:**
   - The `TransactionEncoder` from the `mlxtend` library is used to encode the transactions into a binary matrix format, which is suitable for the Apriori algorithm.

4. **Running Apriori Algorithm:**
   - The Apriori algorithm is applied to the encoded transaction data to find frequent itemsets. A minimum support threshold of 3% is set, meaning that an itemset must appear in at least 3% of transactions to be considered frequent.

5. **Generating Association Rules:**
   - Association rules are generated based on the frequent itemsets using the `association_rules` function from the `mlxtend.frequent_patterns` module. The rules are evaluated based on the **lift** metric, with a threshold of 1.0 for statistical significance.

## **Installation and Requirements**

To run this code, ensure that the following Python libraries are installed:

- `pandas` - For data manipulation and CSV file handling.
- `mlxtend` - For performing the Apriori algorithm and generating association rules.
- `google.colab` - For file uploading in Google Colab.
- `random` - For generating simulated transactional data.
- `io` - For handling the uploaded file.

You can install the required libraries using pip if needed:

```bash
pip install pandas mlxtend
# Market-Basket-Analysis
