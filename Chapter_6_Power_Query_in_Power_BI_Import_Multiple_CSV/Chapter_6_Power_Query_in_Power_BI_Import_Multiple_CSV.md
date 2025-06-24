# 📘 Chapter 6: Access Power Query in Power BI & Import Multiple CSV Files

This chapter covers how to use **Power Query inside Power BI** to import and combine multiple CSV files from a folder — perfect for automating data refresh and analysis.

---

## 🟨 Access Power Query in Power BI

Power Query in Power BI works the same way as in Excel but is embedded in the **Power BI Desktop** tool.

---

## ✅ Steps to Import Multiple CSV Files in Power BI

### 1. 🚀 Open Power BI Desktop
- Launch Power BI Desktop on your system.

---

### 2. 📂 Get Data from Folder
- Click **Home → Get Data → More**
- Choose **Folder** under **File options**
- Click **Connect**

---

### 3. 🔗 Provide Folder Path or URL
- Browse for a local folder **or** paste a shared drive **URL**
- Click **OK** → Then click **Transform Data**

> This opens Power Query Editor showing all files inside the folder.

---

### 4. 🧱 Explore Folder Content
- You’ll see columns like `Content`, `Name`, `Extension`, etc.
- **Remove other columns** and keep only the `Content` column

---

### 5. ➕ Use CSV.Document to Read File Content
- Go to **Add Column → Custom Column**
- Name it `ParsedCSV`
- Use the formula:

  ```powerquery
  Csv.Document([Content])

---
  
### 6. ⏷ Expand the Data
Click the expand icon (⏷) next to the ParsedCSV column

Select all relevant columns

Uncheck "Use original column name as prefix"

---

### 7. 🏷️ Promote Headers (Optional)
If the first row of data is the header, go to:

Transform → Use First Row as Headers

---

### 8. ✅ Load Data into Power BI
Once cleaned, click:

Home → Close & Apply

Power BI loads the data into the model for visualization

---

### 💡 Bonus Tip
You can refresh the dataset anytime by just dropping new CSV files into the folder.

Then click Refresh in Power BI to update your reports
