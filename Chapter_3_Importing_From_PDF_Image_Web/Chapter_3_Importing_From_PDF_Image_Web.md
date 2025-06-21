# Chapter 3: Importing Data from PDF, Image, and Website in Excel Power Query

Excel Power Query allows us to pull data not just from Excel or CSV files, but also from PDFs, images, and even websites. This chapter covers how to import from these three different sources.

---

## 📄 1. Importing Data from a PDF File

### Steps:
1. Go to **Data** tab → Click **Get Data** → **From File** → **From PDF**
2. Select the PDF file from your system.
3. The **Navigator** window opens, showing tables and pages.
4. Choose the relevant table or page.
5. Click **Transform Data** to make edits, or **Load** to import directly.
6. Click **Close & Load** to bring it into Excel.

✅ *Use Transform Data if you want to clean the data first.*

---

## 🖼️ 2. Importing Data from an Image

> This feature is available in **Excel 365** or the **Excel Mobile app**.

### Steps (on supported Excel versions):
1. Go to the **Insert** tab → Click **Data from Picture**.
2. Upload or capture an image containing tabular data.
3. Excel will process it using OCR (Optical Character Recognition).
4. Review the detected values and correct any errors.
5. Click **Insert** to add the data as a table.

✅ *Useful for scanned bills, printouts, or handwritten notes (if clear).*

---

## 🌐 3. Importing Data from a Website

### Steps:
1. Go to **Data** tab → **Get Data** → **From Other Sources** → **From Web**
2. Enter the full website URL (e.g., `https://www.worldometers.info/world-population/`)
3. Wait for the **Navigator** to load tables from the page.
4. Select the desired table.
5. Click **Transform Data** to clean it up.
6. Then click **Close & Load**.

✅ *Best for static HTML tables. May not work well for dynamic websites with JavaScript content.*

---

## 📌 Summary Tips

- Always prefer **Transform Data** to clean before loading.
- PDF import works well for structured reports.
- Image import requires clear text for accuracy.
- Web import is fast but needs a clean table format on the site.

---

## 💡 Bonus: Auto Refresh

For regularly updated sources (PDF or Web):
- Save the query.
- Use **Data → Refresh All** to get the latest data without repeating steps.

