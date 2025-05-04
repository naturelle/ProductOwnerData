# ProductOwnerData
Daily transaction data validation pipeline for an online mart, including error detection, logging, and reporting.

# Transaction Data Validator

This project implements a data validation pipeline for a fictional online marketplace. It processes and validates daily transaction files related to orders, products, and error logs. The goal is to ensure data integrity, generate error reports, and categorize records as successful or rejected.

## 📁 Input Files

The script works with three daily input files:
- `orders.csv`: Contains order records.
- `product_master.csv`: Contains valid product information.
- `error_orders.csv`: Contains pre-identified erroneous entries.

## 🛠️ Features

- Validates each order entry against product master data.
- Automatically segregates valid and invalid orders into respective folders.
- Logs detailed error messages for rejected orders.
- Sends a summary report by email (optional or customizable).
- Supports daily file processing in an automated or batch fashion.

## 📊 Output

- `success/`: Folder containing successfully validated records.
- `reject/`: Folder containing invalid records with error logs.
- `logs/`: Detailed log file describing reasons for rejection.
- (Optional) Summary email report sent to stakeholders.

## 🚀 Technologies Used

- Python (Pandas, os, datetime)
- Logging
- File and folder handling
- Email (SMTP) — optional, for report dispatching

## 📌 Future Enhancements

- Integration with databases instead of flat files
- Scheduled automation (e.g., using cron or Airflow)
- Real-time validation via webhooks or APIs

## 📂 Project Structure
validator/
│
├── input/
│ ├── orders.csv
│ ├── product_master.csv
│ └── error_orders.csv
│
├── success/
├── reject/
├── logs/
├── validator.py
└── README.md
## 🧪 How to Run

1. Place your input files in the `input/` folder.
2. Run the script:
```bash
python validator.py

