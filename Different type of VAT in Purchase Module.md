In an ERP system, each type of VAT in procurement should be mapped to specific chart of accounts (COA) for accurate accounting, compliance, and reporting. Below is a breakdown of the accounting treatment and ledger types for each VAT category involved in procurement.

# 🔶 Chart of Accounts for VAT in Procurement

| **VAT Type**                  | **Account Name**                       | **Account Type**     | **Nature**       | **Rebatable?** | **Accounting Ledger Purpose**                    |
| ----------------------------- | -------------------------------------- | -------------------- | ---------------- | -------------- | ------------------------------------------------ |
| **1. Input VAT**              | Input VAT Receivable (Local)           | Current Asset        | Debit            | ✅ Yes          | To claim VAT credit on purchases                 |
| **2. Input VAT on Import**    | Input VAT Receivable (Import)          | Current Asset        | Debit            | ✅ Yes          | AVAT paid at import stage, creditable            |
| **3. VAT Deducted at Source** | VAT Payable Withholding / VDS Payable  | Current Liability    | Credit (Interim) | ✅ Yes          | Deducted VAT to be deposited to NBR              |
| **4. Non-rebatable VAT**      | VAT Expense (Non-rebatable)            | Expense              | Debit            | ❌ No           | Treated as cost/expense since not creditable     |
| **5. Turnover VAT**           | VAT Expense (Embedded/Turnover Vendor) | Expense              | Debit            | ❌ No           | Treated as part of purchase price, not claimable |
| **6. Mushak-based VAT**       | Input VAT Receivable (Mushak 6.3)      | Current Asset        | Debit            | ✅ Yes          | For purchases from VAT-registered suppliers      |
| **7. Supplementary Duty**     | Supplementary Duty (SD) Expense/Tax    | Expense or Liability | Debit            | ❌ No           | Treated as cost or tax depending on context      |

# 🔷 Example ERP Journal Entries
## ✅ 1. Purchase with Rebatable VAT (Local)

| Date       | Account Name                | Debit (৳) | Credit (৳) |
| ---------- | --------------------------- | --------- | ---------- |
| xx/xx/xxxx | Office Furniture Expense    | 10,000    |            |
|            | VAT Expense (Non-rebatable) | 1,500     |            |
|            | Accounts Payable (Vendor)   |           | 11,500     |

## ❌ 2. Purchase with Non-Rebatable VAT
| Date       | Account Name                | Debit (৳) | Credit (৳) |
| ---------- | --------------------------- | --------- | ---------- |
| xx/xx/xxxx | Office Furniture Expense    | 10,000    |            |
|            | VAT Expense (Non-rebatable) | 1,500     |            |
|            | Accounts Payable (Vendor)   |           | 11,500     |

## 🚢 3. Import Purchase with Advance VAT (AVAT)

| Date       | Account Name                  | Debit (৳) | Credit (৳) |
| ---------- | ----------------------------- | --------- | ---------- |
| xx/xx/xxxx | Goods in Transit              | 10,000    |            |
|            | Input VAT Receivable (Import) | 1,500     |            |
|            | Customs Duty Payable          | 500       |            |
|            | Bank (LC Margin Paid)         |           | 12,000     |

## 🧾 4. Procurement with VDS (VAT Deducted at Source)
| Date       | Account Name         | Debit (৳) | Credit (৳) |
| ---------- | -------------------- | --------- | ---------- |
| xx/xx/xxxx | Service Expense      | 10,000    |            |
|            | VDS Payable          |           | 1,500      |
|            | Bank/Cash (Net Paid) |           | 8,500      |

## ✅ ERP System Ledger Mapping Best Practice

| **ERP Module**  | **Ledger/COA Name**                 | **Type**  |
| --------------- | ----------------------------------- | --------- |
| Purchase Module | Inventory or Expense Accounts       | Debit     |
| Purchase Module | Input VAT Receivable (Local/Import) | Debit     |
| Tax Module      | VAT Payable (VDS)                   | Credit    |
| Import Module   | AVAT / SD Payable / Customs Payable | Liability |
| Finance Module  | Bank/Cash                           | Credit    |
| GL Module       | Vendor Control                      | Credit    |


