# Wallet Credit Scoring using Aave V2 Transactions

## 🌟 Objective
Assign a credit score between **0 and 1000** to wallets based on their historical behavior on the **Aave V2 DeFi protocol**, using transaction-level data.

---

## ⚙️ Overview of the Solution
This solution analyzes raw transaction logs from Aave V2, groups them by wallet, extracts behavioral and financial features, and then scores each wallet using normalized feature values.

---

## 🔄 Workflow

1. **Load JSON**: Flat transaction records are loaded from `user_transactions.json`.
2. **Group by Wallet**: Transactions are grouped by `userWallet`.
3. **Feature Extraction**:
   - Transaction counts and amounts for key actions.
   - Time gap between actions.
   - Duration of activity (active days).
   - Ratios: repay/borrow, redeem/deposit.
4. **Scoring Logic**:
   - Features are normalized using `MinMaxScaler`.
   - Final credit score = mean of normalized features × 1000.
5. **Save Output**: Results saved to `wallet_scores.csv`.

---

## 🔢 Features Used

| Feature                  | Description                                     |
|--------------------------|-------------------------------------------------|
| `count_deposit`          | Number of deposits made                         |
| `total_deposit`          | Total value deposited                           |
| `count_borrow`           | Number of borrow actions                        |
| `repay_borrow_ratio`     | Ratio of repaid vs borrowed amount              |
| `redeem_deposit_ratio`   | Ratio of redeemed vs deposited amount           |
| `avg_time_gap`           | Average time between transactions (seconds)     |
| `active_days`            | Days between first and last activity            |
| `count_liquidationcall`  | Number of times user was liquidated             |

---

## 🧰 How to Run

### Locally
```bash
pip install pandas scikit-learn
python score_wallets.py
