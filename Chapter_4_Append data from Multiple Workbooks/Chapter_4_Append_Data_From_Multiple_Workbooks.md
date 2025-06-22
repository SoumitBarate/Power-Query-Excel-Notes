# Chapter 4: Append Data from Multiple Excel Workbooks using Power Query

Power Query in Excel allows you to combine (append) data from multiple workbooks automatically. This is useful for monthly reports, log files, sales sheets, etc., all having the same structure.

---

## 📂 1. Get Data from a Folder

### Steps:
1. Go to the **Data** tab → Click **Get Data** → **From File** → **From Folder**
2. Select the folder that contains all your Excel files.
3. Click **Transform Data** to enter Power Query Editor.

---

## ✂️ 2. Remove Unnecessary Columns

- In the first column (usually named `Content`), **right-click any other column** → Select **Remove Other Columns**
- You should now see only the file path and content in the query.

---

## ➕ 3. Add a Custom Column

- Go to **Add Column** tab → Click **Custom Column**
- Name it something like `GetWorkbook`
- Use this formula:
  ```powerquery
  Excel.Workbook([Content])
