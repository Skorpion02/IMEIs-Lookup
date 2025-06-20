# IMEIs-Lookup

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/Skorpion02/IMEIs-Lookup?logo=github)](https://github.com/Skorpion02/IMEIs-Lookup/commits/main)
[![Issues](https://img.shields.io/github/issues/Skorpion02/IMEIs-Lookup?logo=github)](https://github.com/Skorpion02/IMEIs-Lookup/issues)

> **A tool to process and filter order and stock data from Excel files, allocating available stock to orders according to customizable criteria.**

---

## 🚀 Overview

This project is designed to process and filter data from two Excel files: one for **orders** and another for **stock**. Its main goal is to assign available stock to orders based on criteria like quantity, battery condition, and product grade.

---

## ✨ Main Features

- **Excel File Loader:** Reads order and stock files into `pandas.DataFrame`.
- **Column Normalization:** Standardizes column names (lowercase, no spaces).
- **Grade Mapping:** Converts grade values (`a`, `b`, `c`) into (`mint`, `good`, `fair`).
- **Advanced Filtering:** Filters stock based on order requirements for quantity and battery condition, notifies about unfulfilled orders, and calculates total missing units.
- **Column Selection:** Allows selection of only the necessary columns for the final output.
- **Export Results:** Saves the result to a new Excel file.

---

## 🛠️ Usage Example

```python
# Load files
df_order, df_stock = load_excel_files("orders.xlsx", "stock.xlsx")

# Normalize columns
df_order = normalize_columns(df_order, "column_name")
df_stock = normalize_columns(df_stock, "column_name")

# Map grades
df_stock = map_grades(df_stock, "grade_column")

# Filter by quantity and battery
result, missing = filter_by_qty_and_battery(df_order, df_stock)

# Select columns and save
result = select_columns(result, ["col1", "col2", "col3"])
save_to_excel(result, "results.xlsx")
```

---

## 📂 Main Workflow

1. **Load** the order and stock files.
2. **Normalize** and **map** the necessary columns.
3. **Filter** and **assign** stock to orders.
4. **Save** the results to an Excel file.

---

## 📋 Requirements

- Python 3.9+
- pandas
- openpyxl (for Excel support)

Install dependencies with:

```bash
pip install pandas openpyxl
```

---

## 🤝 Contributions

Contributions, issues, and suggestions are welcome! Open an [issue](https://github.com/Skorpion02/IMEIs-Lookup/issues) or a pull request.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
