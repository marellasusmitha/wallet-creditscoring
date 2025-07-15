 🚀 Note: I'm new to blockchain but excited to explore and grow in this space!

# Wallet Credit Scoring System – Zeru Assignment

## Problem Statement
The goal of this assignment was to build a machine learning model that assigns a credit score (from 0 to 1000) to each wallet based on how it interacts with the Aave V2 DeFi protocol.

Wallets perform actions like `deposit`, `borrow`, `repay`, `redeemunderlying`, and `liquidationcall`. Based on this behavior, the idea is to score how trustworthy or risky the wallet is.

## My Approach
🔹 Step 1: Data Loading
- I loaded the raw transaction data from the provided JSON file into a pandas DataFrame using Python.
- Each row represents one wallet transaction.
🔹 Step 2: Feature Engineering
For each wallet, I calculated:
- Number of `deposits`, `borrows`, `repays`, `redeems`, and `liquidations`
- `Repay Ratio` (repay_count / borrow_count)
- `Risk Factor` (liquidation_count / total transactions)
These features help understand whether a wallet behaves responsibly or not.
🔹 Step 3: Model Training
- I used a **Random Forest Regressor** to assign scores based on the features.
- Then I scaled the scores between 0 and 1000 using **MinMaxScaler**.
🔹 Step 4: Output
- The final scores were saved in a file called `wallet_scores.json` in the required format.

## Files in This Repo

- main.ipynb: My notebook with all the steps above
- wallet_scores.json: Final output file with scores
- README.md: This file
- analysis.md: Contains graphs(Histogram) and behavior analysis based on wallet scores

## ⚙️ How to Run

You can run the code in Google Colab or Jupyter Notebook.

## Tools Used
- Python
- pandas
- scikit-learn
- matplotlib

## ✅ Conclusion

This project helped me understand how to analyze blockchain transactions and apply machine learning to assign trust scores to users. The scoring system can help DeFi platforms offer credit-based lending without relying on heavy collateral.

**This project was my first hands-on experience working with blockchain-based data, and I really enjoyed it. I'm new to DeFi and blockchain concepts, but through this assignment, I got a better understanding of how wallet transactions work and how machine learning can be used to solve real-world problems like credit scoring.I'm genuinely interested in learning more about blockchain and DeFi, and I see this opportunity as a great starting point in that direction. Thank you for the chance to work on this!
