# Chapter 2: Importing Large CSV Files in Power Query

Working with large CSV files (hundreds of MBs or even GBs) can slow down Excel. Power Query offers efficient ways to handle them without crashing your system.

---

## 📂 Steps to Import a Large CSV File

### 1. Open Excel → Go to **Data** Tab
- Click **Get Data** → **From File** → **From Text/CSV**

---

### 2. Select the Large CSV File
- Wait for the preview to load (may take a few seconds).
- Click **Transform Data** (don’t use "Load" directly for large files).

---

### 3. Use **Transform Data** Instead of **Load**
- This opens the Power Query Editor where you can filter, reduce, and preview only required data before loading it fully into Excel.

---

## 🧹 Tips to Handle Large Files Efficiently

### ✅ Reduce Data Before Loading
- Filter out unnecessary rows or columns.
- Keep only the required columns.
- Use **Remove Other Columns** to limit memory usage.

---

### ✅ Disable Auto Data Type Detection
- Go to **File → Options → Query Options → Data Load**
- Uncheck **Automatically detect column types**
- This speeds up preview and transformation.

---

### ✅ Load to Connection Only (Optional)
- After cleaning, click **Close & Load To…**
- Select **Only Create Connection** or **Load to Data Model**
- This avoids overloading Excel sheets with rows.

---

## ⚙️ Advanced Tip: Use CSV Import with Power BI or Split File

- If file is too large for Excel, consider:
  - Importing in **Power BI Desktop**
  - Splitting CSV into parts using tools like Python, Notepad++, or PowerShell
  - Using Power Query parameters to process chunks

---

## 📌 Final Advice

- Avoid loading unnecessary data.
- Always transform before load.
- If it feels slow, consider upgrading to 64-bit Excel or moving to Power BI.

