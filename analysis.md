# Analysis of Wallet Credit Scores

## 🔹 Score Distribution (Buckets of 100)

Below is the **real distribution** after scoring all wallets:

| Score Range | Wallet Count |
|-------------|--------------|
| 0-100       | 1929         |
| 100-200     | 112          |
| 200-300     | 6            |
| 300-400     | 1            |
| 400-500     | 0            |
| 500-600     | 0            |
| 600-700     | 0            |
| 700-800     | 0            |
| 800-900     | 0            |
| 900-1000    | 0            |

---

## 🤔 Observations

### 🔴 Low Score Wallets (0–400):
- Frequent `borrow` transactions with little or no `repay`
- Many `liquidationcall` entries
- Often active for a short duration (few days)
- Small or no `deposit` actions
- Indicate risky, bot-like, or spammy usage

### 🔵 High Score Wallets (800–1000):
- Balanced `deposit`, `borrow`, and `repay` activity
- High `repay/borrow` and `redeem/deposit` ratios
- Long active period across time (more than 90 days)
- No or very few `liquidationcall`
- Indicate responsible and reliable DeFi participation
