# 🧾  Purchase Accounting Logic (VAT-Inclusive with TDS Deduction)

This section outlines how to account for a supplier purchase when the total amount includes VAT and TDS is applicable.

## 💡 Scenario:
- **Total Purchase Amount**: BDT 1,000 (VAT inclusive)  
- **VAT Rate**: 15%  
- **TDS Rate**: 5% (on the net amount excluding VAT)
---

## 📊 Calculation Breakdown:
1. **Net Purchase Amount (Excluding VAT)**  
   ```
   Net Amount = 1000 / 1.15 = 869.57
   ```
2. **VAT Component**  
   ```
   VAT = 1000 - 869.57 = 130.43
   ```
3. **TDS Deduction (5% on Net Amount)**  
   ```
   TDS = 5% × 869.57 = 43.48
   ```
4. **Amount Payable to Supplier**  
   ```
   Payable = 1000 - 43.48 = 956.52
   ```
---

## 📘 Journal Entry: If purchase is for resale/manufacture: Inventory will be (Asset).

| Particulars             | Debit (BDT) | Credit (BDT) | Account Type                         |
| ----------------------- | ----------- | ------------ | ------------------------------------ |
| **Inventory Account**   | 869.57      |              | Asset (Current Asset)                |
| **VAT Input Account**   | 130.43      |              | Asset (Recoverable/Revatable Tax)    |
| To **Supplier Payable** |             | 956.52       | Liability                            |
| To **TDS Payable (5%)** |             | 43.48        | Liability (Statutory Dues)           |

## 📘 Journal Entry: If purchase is for direct use/consumption: Use Purchase (Expense).

| Particulars             | Debit (BDT) | Credit (BDT) | Account Type                         |
| ----------------------- | ----------- | ------------ | ------------------------------------ |
| **Purchase Account**    | 869.57      |              | Expense (Current Asset)                |
| **VAT Input Account**   | 130.43      |              | Asset (Recoverable/Revatable Tax)    |
| To **Supplier Payable** |             | 956.52       | Liability                            |
| To **TDS Payable (5%)** |             | 43.48        | Liability (Statutory Dues)           |


> **Note:** This entry reflects a typical purchase transaction where the gross invoice amount includes VAT, and TDS is withheld before payment to the supplier.
