# Wallet CreditScoring– Zeru Assignment

After generating the credit scores for wallets, I plotted the score distribution using a histogram with bins from 0 to 1000 (in 100-point intervals). The output graph showed that the majority of the wallets fall under the 0–100 score range.

## 🔹 Score Distribution Observation


- Around **3500+ wallets** are in the **0–100** range.
- Almost no wallets scored above 200.
- The distribution is extremely skewed towards the low end.

This suggests that most wallets either had:
- No repayment behavior,
- High liquidation ratios,
- Very limited or one-sided interactions (like borrowing without repaying).

## 🔍 Score Range Behavior Analysis

🔴 0–100 (Most wallets):
- These wallets were either highly inactive or showed risky behavior.
- They typically borrowed and either didn’t repay or were liquidated.
- May include spam, bot accounts, or one-time exploiters.

🟠 100–300 (Very few):
- Wallets that interacted more, but either repaid partially or inconsistently.
- A step up from the riskiest, but still not highly trustworthy.

🟢 700–1000 (Almost none):
- These would be the ideal wallets with clean behavior: multiple borrows, consistent repayments, and no liquidations.
- Very rare in this dataset, possibly due to how features or scoring were weighted.

## 📈Takeaways
- Most wallets on-chain are not behaving in a highly responsible way, which is a common challenge in DeFi.
- It highlights the need for robust scoring models like this to separate trusted users from risky ones.
- This model worked well in identifying and penalizing risky behaviors.
  
### Histogram

<img width="860" height="621" alt="Screenshot 2025-07-15 192058" src="https://github.com/user-attachments/assets/ca6c00dd-bae7-4d8a-88d7-f32617da2f10" />


