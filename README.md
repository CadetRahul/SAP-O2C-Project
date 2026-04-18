# 💼 SAP SD — Order-to-Cash (O2C) Process Implementation

> **Mini Project | ERP Systems | KIIT University | 2024-25**

---

## 📋 Project Overview

This project demonstrates the **complete Order-to-Cash (O2C)** business process implemented using **SAP S/4HANA Sales & Distribution (SD)** module.

The O2C cycle automates the entire sales workflow — from the moment a customer places an inquiry to the final payment receipt — integrating SAP SD, MM (Materials Management), and FI (Finance) modules seamlessly.

---

## 🔄 O2C Process Flow

```
Customer Inquiry (VA11)
        ↓
Quotation (VA21)
        ↓
Sales Order (VA01)  ← CORE DOCUMENT
        ↓
Delivery Processing (VL01N)
        ↓
Goods Issue (VL02N)  ← Inventory reduced
        ↓
Billing / Invoice (VF01)  ← FI posting auto
        ↓
Payment Receipt (F-28)  ← AR cleared ✔
```

---

## 🛠️ Technology Stack

| Component | Technology |
|-----------|-----------|
| ERP Platform | SAP S/4HANA |
| SAP Module | Sales & Distribution (SD) |
| Integration | SAP MM + SAP FI |
| Database | SAP HANA (In-Memory) |
| UI | SAP GUI / SAP Fiori |
| Config Tool | SAP SPRO (IMG) |

---

## 📁 Project Structure

```
SAP_O2C_Project/
├── README.md                    ← This file
├── docs/
│   ├── O2C_Process_Flow.md      ← Detailed step-by-step guide
│   ├── SAP_Configuration.md     ← SPRO config guide
│   └── Transaction_Codes.md     ← All T-codes reference
├── screenshots/
│   ├── 01_customer_inquiry.png
│   ├── 02_quotation.png
│   ├── 03_sales_order.png
│   ├── 04_delivery.png
│   ├── 05_goods_issue.png
│   ├── 06_billing.png
│   └── 07_payment.png
├── config/
│   └── master_data_setup.md     ← Customer & material master setup
└── scripts/
    └── test_scenarios.md        ← Sample test cases
```

---

## ⚡ Key Features

- ✅ **Full automation** — zero manual intervention between steps
- ✅ **Real-time inventory** update on Goods Issue
- ✅ **Auto billing** immediately after GI
- ✅ **Complete document flow** — all 7 docs linked
- ✅ **Credit check** — auto block if limit exceeded
- ✅ **Multi-module integration** — SD + MM + FI

---

## 📊 Transaction Codes Quick Reference

| Step | T-Code | Description |
|------|--------|-------------|
| Inquiry | VA11 | Create Customer Inquiry |
| Quotation | VA21 | Create Quotation |
| Sales Order | VA01 | Create Sales Order |
| Delivery | VL01N | Create Outbound Delivery |
| Goods Issue | VL02N | Post Goods Issue |
| Billing | VF01 | Create Billing Document |
| Payment | F-28 | Post Incoming Payment |
| Doc Flow | VA03 | View Document Flow |

---

## 👨‍💻 Team & Institution

**Institution:** Kalinga Institute of Industrial Technology (KIIT), Bhubaneswar  
**Course:** ERP Systems / SAP SD  
**Academic Year:** 2024 – 2025  

---

## 📄 Project Report

See `SAP_O2C_Project_Report.pdf` for the complete project documentation.
