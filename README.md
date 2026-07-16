# Project 1: Data Cleaning & Preparation
**Company:** DecodeLabs | **Track:** Data Analytics | **Batch:** 2026

## Goal
Clean a raw e-commerce orders dataset by handling missing values, duplicates, and incorrect data formats — proving mastery of data integrity fundamentals before moving to analysis/modeling.

## Dataset
`raw_dataset.xlsx` — real dataset provided by DecodeLabs (1,200 orders, 14 columns): OrderID, Date, CustomerID, Product, Quantity, UnitPrice, ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber, ItemsInCart, CouponCode, ReferralSource, TotalPrice.

## Tech Stack
Python, pandas, Jupyter Notebook, reportlab (for the PDF change log)

## Files
- `Data_Cleaning_Preparation.ipynb` — full cleaning pipeline (executed, with outputs)
- `raw_dataset.xlsx` — original provided dataset
- `cleaned_dataset.xlsx` / `cleaned_dataset.csv` — final, cleaned, production-ready dataset
- `Change_Log.pdf` — formal change log documenting every modification (Change ID, Description, Impact, Status) as required by the project brief

## Key Requirements Met
- ✅ Identified missing/null values — `CouponCode` (309 missing) imputed with explicit `'NoCoupon'` label
- ✅ Verified zero exact duplicate rows
- ✅ Verified **0% error rate** on unique identifiers (OrderID, TrackingNumber — both 100% unique)
- ✅ Verified **0% error rate** on date formats — all dates standardised to ISO 8601 (`YYYY-MM-DD`)
- ✅ Standardised text formatting (whitespace trimmed, consistent casing) across 6 categorical columns
- ✅ Numeric precision enforced (2 decimal places on currency fields)
- ✅ Cross-validated `TotalPrice = Quantity × UnitPrice` business logic
- ✅ Outlier detection via IQR method — flagged (not deleted) for transparency
- ✅ Data types corrected for reliable downstream analysis
- ✅ Full change log documented in `Change_Log.pdf` (required deliverable per project brief)

## How to Run
```
pip install pandas numpy openpyxl reportlab
jupyter notebook Data_Cleaning_Preparation.ipynb
```

## Author
DecodeLabs Data Analytics Intern — Project 1
