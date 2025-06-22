# 📘 Chapter 4: Append Data from Multiple Excel Workbooks using Power Query

Appending data from multiple Excel workbooks in a folder helps automate data consolidation. Power Query provides a simple and efficient way to do this inside Excel.

---

## ✅ Steps to Append Data from Multiple Workbooks

### 1. 📂 Get Data from Folder
- Open Excel.
- Go to the **Data** tab → Click **Get Data** → **From File** → **From Folder**.
- Select the folder that contains all the Excel files.
- Click **OK**, then choose **Transform Data** (not Load).

> Power Query will list all files in that folder.

---

### 2. ✂️ Remove Other Columns
- In Power Query Editor, you’ll see columns like `Name`, `Extension`, `Date accessed`, and `Content`.
- **Right-click on the `Content` column** → Select **Remove Other Columns**.

> Now only the `Content` column remains, which contains the binary file content of each Excel file.

---

### 3. ➕ Add a Custom Column
- Go to the **Add Column** tab → Click **Custom Column**.
- Name the new column as: `GetWorkbook`
- Use the following formula:

  ```powerquery
  Excel.Workbook([Content])
This will extract the internal tables and sheets from each workbook.

---

### 4. 🗑️ Delete the First Column
Right-click the original Content column.

Select Remove to keep only the new column with workbook structures.

---

### 5. ⏷ Expand the Table
Click the expand icon (⏷) next to the GetWorkbook column.

Select the fields you need:

Data (actual data table),

Name (name of sheet or table),

Kind (Sheet, Table, NamedRange, etc.)

Uncheck "Use original column name as prefix"

Click OK.

---

### 6. 🏷️ Promote Headers (Optional)
If the imported data has headers in the first row, promote them to actual headers using a custom column.

Go to Add Column → Custom Column

Use the following formula:

powerquery
Copy
Edit
Table.PromoteHeaders([Data.1])
This makes the first row of each imported table act as the column headers.

---

### 7. ✅ Final Load
Once data is expanded and cleaned, click:

Home tab → Close & Load

Choose to load to Excel worksheet or Data Model
