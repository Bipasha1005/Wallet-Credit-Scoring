# Wallet Credit Scoring using Aave V2 DeFi Transactions

## 🎯 Objective

Assign credit scores (0–1000) to wallets based on responsible usage of Aave V2 protocol using ML and behavior-driven analytics.

---

## ⚙️ How It Works

1. **Data Parsing**: Reads a large JSON file with transaction-level details.
2. **Feature Engineering**:
   - Transaction counts and amounts for each action type.
   - Behavior metrics: time gaps, active days.
   - Risk indicators: liquidation, repayment ratio.
3. **Scoring**:
   - Features normalized using MinMaxScaler.
   - Scores assigned by mean of normalized metrics × 1000.

---

## 🧪 Running the Code

```bash
python score_wallets.py
