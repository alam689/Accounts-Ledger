
# 📦 Bill of Entry (BOE) Calculation in Bangladesh

This guide explains how to calculate the Bill of Entry (BOE) for import purchases in Bangladesh under the VAT and Customs regulations.

---

## ✅ Step-by-Step BOE Calculation

### Assumptions:
- **Invoice Value (CFR/C&F)** = USD 10,000  
- **Exchange Rate** = 110 BDT/USD  
- **Assessable Value (AV)** = 10,000 × 110 = **BDT 1,100,000**

---

### 🧮 BOE Components:

| Component                        | Rate / Formula                             | Amount (BDT)              |
|----------------------------------|--------------------------------------------|---------------------------|
| **1. Assessable Value (AV)**     | Invoice Value × Exchange Rate              | 1,100,000                 |
| **2. Customs Duty (CD)**         | AV × CD rate (e.g., 10%)                   | 110,000                   |
| **3. Regulatory Duty (RD)**      | (AV + CD) × RD rate (e.g., 3%)             | 36,300                    |
| **4. Supplementary Duty (SD)**   | (AV + CD + RD) × SD rate (e.g., 20%)       | 249,260                   |
| **5. VAT**                       | (AV + CD + RD + SD) × 15%                  | 216,789                   |
| **6. Advance Income Tax (AIT)**  | AV × 5%                                    | 55,000                    |
| **7. Advance Trade VAT (ATV)**   | AV × 4% (if applicable)                    | 44,000                    |

---

### 📊 Total Tax Payable:
**Total Tax = CD + RD + SD + VAT + AIT (+ ATV if applicable)**  
**Total = 110,000 + 36,300 + 249,260 + 216,789 + 55,000 + 44,000 = BDT 711,349**

---

## 🧾 Landed Cost Calculation:

If additional charges are:
- **Port/CHA Charges**: BDT 20,000  
- **Transport**: BDT 10,000  

Then:  
**Landed Cost = AV + Total Taxes + Other Charges**  
**= 1,100,000 + 711,349 + 20,000 + 10,000 = BDT 1,841,349**

---

## 📑 BOE Documentation Checklist:
- Invoice & Packing List  
- Bill of Lading  
- LC Copy  
- Import Permit & HS Code  
- Tax Breakdown (CD, RD, SD, VAT, AIT)  
- Bank Endorsement (for LC)

---

## 📂 Usage

You can use this markdown file as a base reference or for training, ERP documentation, or BOE audit trails.

# 📘 BOE Components with Account Type Classification

| Component                    | Example Entry (BDT) | Account Name               | Account Type            | Notes                                   |
| ---------------------------- | ------------------- | -------------------------- | ----------------------- | --------------------------------------- |
| **Assessable Value (AV)**    | 1,100,000           | Inventory / Raw Materials  | **Asset**               | Capitalized in inventory                |
| **Customs Duty (CD)**        | 110,000             | Customs Duty Payable       | **Liability / Expense** | Can be expense or part of inventory     |
| **Regulatory Duty (RD)**     | 36,300              | Regulatory Duty Payable    | **Liability / Expense** | Similar to CD, usually included in cost |
| **Supplementary Duty (SD)**  | 249,260             | Supplementary Duty Payable | **Liability / Expense** | Add to inventory value                  |
| **VAT at Import**            | 216,789             | **VAT Input (Import)**     | **Asset**               | Claimable input VAT                     |
| **Advance Income Tax (AIT)** | 55,000              | **Advance Tax (AIT)**      | **Asset**               | Considered an advance income tax asset  |
| **Advance Trade VAT (ATV)**  | 44,000              | Advance Trade VAT          | **Asset**               | Claimable or adjustable                 |
| **Port Charges**             | 20,000              | Port / CHA Expense         | **Expense or Asset**    | Add to inventory if material            |
| **Transport/Local Delivery** | 10,000              | Transport Inward (Import)  | **Expense or Asset**    | Add to inventory for landed cost        |

# 📦 Inventory Capitalization:
All costs directly attributable to getting the goods to their intended location and condition should be capitalized in inventory (as per IAS 2 or local GAAP).
Therefore, CD, RD, SD, VAT (if non-creditable), Port Charges, Transport are typically added to inventory cost.
# 🧾 ERP Journal Entry Summary Example
| Account                            | Type      | Debit (BDT) | Credit (BDT) |
| ---------------------------------- | --------- | ----------- | ------------ |
| Inventory / Raw Materials          | Asset     | 1,841,349   |              |
| VAT Input (Import)                 | Asset     | 216,789     |              |
| Advance Tax (AIT)                  | Asset     | 55,000      |              |
| LC / Foreign Supplier Payable      | Liability |             | 1,100,000    |
| Customs, RD, SD Payable (Optional) | Liability |             | 395,560      |
| Bank / Cash                        | Asset     |             | 617,578      |


