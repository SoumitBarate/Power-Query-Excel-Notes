# Data Cleaning in Power Query

Data cleaning is a crucial step in preparing your dataset for analysis. Power Query in Excel provides powerful tools to clean, transform, and prepare data for downstream processing and visualization.

---

## 🧹 Common Data Cleaning Steps

### 1. Remove Blank Rows
- Navigate to the **Home** tab in the Power Query Editor.
- Click on **Remove Rows** → Select **Remove Blank Rows**.
- You can also use **Remove Top Rows → 0** if you want to retain all rows initially.

---

### 2. Join Two Columns (e.g., First Name + Last Name)
You can merge two columns using multiple methods:

- **Method 1: Right-Click → Merge Columns**
  - Select both columns (e.g., `FirstName` and `LastName`).
  - Right-click → Select **Merge Columns**.
  - Choose a separator like a space.

- **Method 2: Custom Column**
  - Go to **Add Column** → **Custom Column**.
  - Use this formula:
    ```powerquery
    [FirstName] & " " & [LastName]
    ```

- **Method 3: Column from Example**
  - Go to **Add Column** → **Column from Example**.
  - Manually type the expected merged value to auto-generate logic.

---

### 3. Split One Column into Multiple Columns
- **Right-click** on the target column.
- Select **Split Column** → **By Delimiter**.
- Choose delimiter type (comma, space, custom) and how to split (each occurrence, left-most, right-most).

---

### 4. Handle Null Values
- Discuss the significance of null values with your **team/seniors**.
- Based on the context, you can:
  - Remove rows with nulls: **Home → Remove Rows → Remove Blank Rows**
  - Replace nulls with default values: **Transform → Replace Values**
  - Keep nulls if they're meaningful in the dataset.

---

### 5. Close & Load
- After completing data cleaning:
  - Click **Close & Load** on the Home tab.
  - This will load your cleaned data back into Excel.

---

## 📌 Final Tips
- Always validate your cleaned data against original requirements.
- Make sure no important data is accidentally removed or misinterpreted.
- Document your steps inside Power Query so others can understand your process.

