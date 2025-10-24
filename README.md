# 🧹 Data Cleaning Excel Final Project – **Customer Bike Purchase Dataset**

This repository showcases my **Excel-based data cleaning project**, where I worked on a **real-world customer dataset** related to **bike purchases**.  
The dataset initially had **duplicate records**, **ambiguous abbreviations** (e.g., M/F, S/M), **inconsistent text and date formats**, **currency stored as text** and **categorical ordering issues** (e.g., “10+ miles” sorting before “1–2 miles”).

The goal of this project is to demonstrate my **end-to-end Excel data-cleaning workflow**—transforming raw, inconsistent data into a **clean, analysis-ready** dataset and building **pivot-based dashboards**.

---

## 🎯 **OBJECTIVE**

To **clean and organize** an unstructured customer dataset by:

- **Removing duplicate records** (identified **26 duplicates**)
- **Expanding abbreviations** (e.g., **M → Male**, **F → Female**, **S → Single**, **M → Married**)
- **Standardizing text case** and trimming **extra spaces**
- **Converting currency** from text (with `$`) to true **numeric** values
- **Standardizing date formats**
- **Creating age bands** using a **Nested IF** formula
- **Fixing categorical sort order** (e.g., ensuring **0–1, 1–2, …, 10+ miles**)
- Building **Pivot Tables**, **Charts**, and a **slicer-driven dashboard**

---

## 🧾 **Problem Description**

The **raw dataset** was inconsistent and unsuitable for analysis. Key issues identified:

- **26 duplicate rows** across customer records  
- **Ambiguous abbreviations** (e.g., **M/F** for gender, **S/M** for marital status)  
- **Mixed casing** and **extra spaces** in several columns  
- **Income/Salary** values stored as **text** with symbols like `$`  
- **Inconsistent date patterns** across records  
- **Commute distance** labels causing **wrong alphabetical sorting** (e.g., `10+ miles` appearing before `1–2 miles`)

Because of these issues, the dataset required **significant cleaning** before visualization or reporting.

---

## 🧰 **Tools and Features Used**

All cleaning and analysis were performed in **Microsoft Excel**, using formulas and built-in tools.

### **Excel Features**
- **Remove Duplicates** → detect and eliminate repeated rows  
- **Find & Replace** → expand abbreviations (**M/F**, **S/M**) to full words  
- **Filter & Sort** → surface inconsistencies in categorical fields  
- **Number Formatting** → coerce currency **text** to **numeric**  
- **Date Formatting (Short Date)** → unify inconsistent dates  
- **PivotTable / PivotChart** → aggregate, visualize, and build dashboards  
- **Slicers** → interactive filtering by **Marital Status**, **Education**, **Region**, etc.

### **Excel Formulas**
- `=PROPER(cell)` → standardize **Title Case**  
- `=TRIM(cell)` → remove **leading/trailing/double spaces**  
- **Nested IF (Age Banding):**  
  `=IF([@Age]>54,"Old",IF([@Age]>=31,"Middle Age",IF([@Age]<31,"Adolescent","Invalid")))`

---

## 🪜 **Step-by-Step Cleaning Process**

1. **Deduplicate**  
   - Used **Data → Remove Duplicates**; removed **26** redundant records.

2. **Normalize Text & Abbreviations**  
   - `Find & Replace`: **M → Male**, **F → Female**, **S → Single**, **M → Married** (contextual where column differs).  
   - Applied `PROPER()` to standardize names/labels; used `TRIM()` to clear stray spaces.

3. **Fix Currency & Dates**  
   - Stripped `$` and text artifacts; converted to **Number** with appropriate **Currency** formatting.  
   - Standardized dates via **Short Date** for consistency.

4. **Create Age Bands**  
   - Applied the **Nested IF** above to categorize: **Young**, **Middle Age**, **Old**.  
   - This improved readability and downstream aggregation.

5. **Repair Categorical Order (Commute Distance)**  
   - Adjusted **labeling** so sorting follows **0–1, 1–2, …, 10+ miles** (preventing charts from placing **10+** between small ranges).

6. **Build Pivot Tables**  
   - **Case 1:** Average **Income** by **Gender** and **Bike Purchase (Yes/No)**  
   - **Case 2:** **Commute Distance** vs **Bike Purchase Count**  
   - **Case 3:** **Age Band** vs **Bike Purchase** (banding greatly improved interpretability)

7. **Create Pivot Charts & Dashboard**  
   - Selected best-fit chart types for each case; added **titles**, **axis labels**, and **data tables** where useful.  
   - Added **Slicers** (Marital Status, Education, Region) to enable interactive exploration.  
   - Final dashboard highlights how specific segments (e.g., **Single** + **Bachelor’s**) relate to **purchase behavior**.

---

## 🧩 **Outcome**

- ✅ Dataset is **clean, structured, and analysis-ready**  
- ✅ **Duplicates removed**, **text normalized**, **currency & dates corrected**  
- ✅ **Age bands** and **ordered categories** enable clear, accurate charts  
- ✅ Interactive **Pivot-based dashboard** with **Slicers** for quick insights

---

## 📚 **Learning Reflection**

Through this project, I:

- Practiced **systematic data validation** and **cleaning** with Excel’s built-ins + formulas  
- Learned to **relabel and re-order categories** to avoid misleading visuals  
- Used **PivotTables/Charts** and **Slicers** to go from cleaned data to a **dynamic dashboard**  
- Built a foundation to **scale the same logic** in **Python (Pandas)** / **Power BI** for automation and richer analytics

---

## 📁 **Repository Contents**

- `raw/` → Original **raw data** (Excel)  
- `clean/` → **Cleaned dataset** with standardized schema  
- `pivots/` → **Pivot tables** supporting the dashboard  
- `dashboard/` → Final **dashboard** workbook + screenshots  
- `docs/` → **Step-by-step documentation** of the entire process

> 🔎 Open the `dashboard` workbook and use the **Slicers** to filter by **Marital Status**, **Education**, and **Region**.

---

## 👩‍💻 **Author**

**Soundarya Poovaiah Kookanda**  
📧 **soundaryakookanda@gmail.com**  
🎓 **Master of Engineering in Computer Science — University of Cincinnati**
