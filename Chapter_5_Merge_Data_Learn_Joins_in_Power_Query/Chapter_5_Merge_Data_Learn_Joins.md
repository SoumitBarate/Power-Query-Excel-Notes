# 📘 Chapter 5: Merge Data – Learn Joins in Power Query

This chapter explains how to merge (join) tables in Power Query, understand different types of joins, and how **Merge** differs from **Append**.

---

## 🔄 Append vs Merge: What’s the Difference?

| Feature | Append | Merge |
|--------|--------|-------|
| Combines | Rows (stack vertically) | Columns (side-by-side) |
| When to use | When tables have **same structure** | When tables have **related columns** |
| Example | Combining monthly sales files | Joining customer info with orders |

---

## ✅ Steps to Merge Data Using Joins

### 1. 🚀 Launch Data into Power Query
- Load your Excel tables into Power Query:
  - Select the table → Go to **Data → From Table/Range**

> Repeat for both Table A and Table B.

---

### 2. ➕ Add a Blank Query
- Go to **Home → New Source → Other Sources → Blank Query**

---

### 3. 🔍 Load Existing Tables in Workbook
- In the formula bar of the blank query, type:

  ```powerquery
  =Excel.CurrentWorkbook()

---

### 4. 📝 Duplicate the Tables
Right-click on the original query → Select Duplicate

Name them TableA and TableB for clarity

---

### 5. ✅ Keep Only Relevant Tables
In the Excel.CurrentWorkbook table, remove all rows except for TableA and TableB

---

### 6. 🧹 Clean Up Tables
For both TableA and TableB:

Remove any unwanted columns (e.g., second column)

Keep only the column that will be used as the join key

---

### 7. ⏷ Expand if Needed
If either table has nested columns (like a Table inside a cell):

Click the expand icon (⏷) to flatten the data

---

### 8. 🔗 Merge Tables
Go to Home → Merge Queries (or right-click → Merge)

Select TableA as the first table, and TableB as the second

Choose the matching column (key)

Choose the Join Type:

Inner Join

Left Outer

Right Outer

Full Outer

Anti Joins

Click OK

The result will be a new table with data from both sources joined together.

---

### 🔁 Join Types Quick Reference
Join Type	Description

Inner Join	Only matching rows from both tables

Left Outer Join	All from TableA + matches from TableB

Right Outer Join	All from TableB + matches from TableA

Full Outer Join	All from both tables

Left Anti Join	Rows in TableA not in TableB

Right Anti Join	Rows in TableB not in TableA

✅ Final Step: Load Data
Once merged and cleaned:

Click Home → Close & Load to send data back to Excel

---

### 📌 Summary of Steps

| Step | Action                            |
| ---- | --------------------------------- |
| 1    | Load both tables into Power Query |
| 2    | Add Blank Query                   |
| 3    | Use `Excel.CurrentWorkbook()`     |
| 4    | Duplicate tables                  |
| 5    | Keep only TableA and TableB       |
| 6    | Remove extra columns              |
| 7    | Expand if needed                  |
| 8    | Merge using join types            |
