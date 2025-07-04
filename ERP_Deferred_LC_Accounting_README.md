# 🌐 ERP Import Purchase & Deferred LC Accounting Module

This module handles the end-to-end accounting process for import purchases made under **Deferred Letters of Credit (LCs)**, including **multi-shipment handling**, **cost sheet computation**, and **inventory valuation updates**.

---

## 📦 Key Features

- Manage **LC Opening**, Margin, and Bank Charges
- Handle **Partial Shipment Receipts** (e.g., via Mother & Feeder Vessels)
- Track **Customs Duty, VAT**, and **Port & Transport Expenses**
- Automatically compute **Landed Cost per MT**
- Recognize **Deferred LC Payables** and post **FX Revaluation**
- Generate system journal entries for **Inventory**, **Liabilities**, and **Expenses**
- Integrates with:
  - Inventory
  - Accounts Payable
  - LC & Shipment Tracking
  - Cost Sheet module

---

## 🧾 Example Scenario

| Item                    | Value                              |
|-------------------------|------------------------------------|
| Product                 | Clinker (10,000 MT)                |
| Total Purchase          | $100,000                           |
| Exchange Rate (GRN)     | 1 USD = 110 BDT                    |
| Shipment                | 2 Shipments (5,000 MT each)        |
| Total Local Value       | 11,000,000 BDT                     |
| Import Expenses         | 800,000 BDT                        |
| Final Exchange Rate     | 112 BDT/USD                        |
| Final Payment           | 11,200,000 BDT                     |
| Landed Cost / MT        | 1,180 BDT                          |

---

## 🔁 Step-by-Step ERP Transactions

### 1. LC Opening (Optional)
```text
Dr. LC Margin Deposit (Asset)              1,100,000  
Dr. LC Opening Charges (Expense)              50,000  
    Cr. Bank                                1,150,000
```

---

### 2. First Shipment Received (5,000 MT)
```text
Dr. Inventory – Clinker                     5,500,000  
Dr. Customs Duty & VAT                        200,000  
Dr. Port & Feeder Vessel Charges              200,000  
    Cr. Deferred LC Payable                 5,500,000  
    Cr. Accounts Payable / Bank               400,000
```

---

### 3. Second Shipment Received (5,000 MT)
```text
Dr. Inventory – Clinker                     5,500,000  
Dr. Customs Duty & VAT                        200,000  
Dr. Port & Feeder Vessel Charges              200,000  
    Cr. Deferred LC Payable                 5,500,000  
    Cr. Accounts Payable / Bank               400,000
```

---

### 4. Capitalize Import Costs to Inventory
```text
Dr. Inventory – Clinker (Adjustment)          800,000  
    Cr. Import Charges (Port, Transport)      800,000
```

---

### 5. LC Payment After 90 Days (with Exchange Loss)
```text
Dr. Deferred LC Payable                    11,000,000  
Dr. Exchange Loss                             200,000  
    Cr. Bank                                11,200,000
```

---

### 6. LC Margin Reversal
```text
Dr. Bank                                    1,100,000  
    Cr. LC Margin Deposit                   1,100,000
```

---

## 📊 Final Ledger Summary

| Ledger                         | Amount (BDT) | Type     |
|-------------------------------|---------------|----------|
| Inventory – Clinker           | 11,800,000     | Asset    |
| Deferred LC Payable           | 0              | Liability (Cleared) |
| Bank                          | (11,200,000)   | Asset ↓  |
| LC Margin Deposit             | 0              | Asset (Recovered) |
| Exchange Loss                 | 200,000        | Expense  |

---

## 🛠 ERP Modules Involved

- **LC Master** (Amount, Margin, Maturity)
- **GRN** (Goods Receipt by Shipment)
- **Shipment Tracker** (Mother/Feeder Vessel)
- **Import Cost Sheet** (Landed Cost Calculation)
- **Inventory Valuation** (Actual / Weighted)
- **Accounts Payable** (for Charges & Vendors)
- **Journal Voucher** (Automated GL Posting)

---

## 📁 Folder Structure Suggestion

```plaintext
erp_import_lc/
├── models/
│   ├── lc_master.py
│   ├── shipment.py
│   ├── cost_sheet.py
│   └── journal.py
├── services/
│   ├── landed_cost_calculator.py
│   └── fx_revaluation.py
├── reports/
│   ├── cost_sheet_summary.xlsx
│   └── shipment_register.pdf
└── README.md
```

---

## 📞 Contact & Contribution

For enhancements, issue tracking, or customization:
- 📧 Email: your-email@example.com
- 🏢 Organization: [Your Company Name]
- 🛠 Contributions welcome via pull requests

---

> ⚠️ **Note**: This is a simplified accounting model. Actual implementation should be aligned with your national import regulations and accounting standards (e.g., IAS 2, IAS 21).
