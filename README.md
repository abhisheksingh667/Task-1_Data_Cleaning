# Task 01 – Data Cleaning and Preprocessing  
**Internship: Data Analytics – Skilllytics**

## 📌 Objective  
Clean and preprocess the Medical Appointment No-Show dataset to prepare it for further analysis.

---

## 📂 Dataset Used  
**Dataset:** Medical Appointment No-Show (KaggleV2-May-2016.csv)  
**Rows:** ~110,527  
**Columns:** 14 (raw) + 1 added column (waiting_day)

---

## 🧹 Cleaning Steps Performed

### 1️⃣ Removed Duplicates  
- Used Excel → Data → Remove Duplicates  
- Removed all fully duplicate records.

### 2️⃣ Fixed Invalid Age Values  
- Found rows with `age = -1` (invalid).  
- Deleted those rows completely.  
- Ensured age contains only valid non-negative integers.

### 3️⃣ Cleaned Date Columns  
- Original format: `2016-04-29T18:38:08Z`  
- Extracted only date portion using:  
  - `=DATEVALUE(LEFT(cell,10))`  
- Converted ScheduledDay and AppointmentDay into proper Excel date format.

### 4️⃣ Added New Derived Column  
**waiting_day = appointment_day – scheduled_day**  
- Shows number of days between scheduling and actual appointment.

### 5️⃣ Cleaned & Standardized Gender  
- Replaced M → Male  
- Replaced F → Female  
- Removed incorrect replacements.

### 6️⃣ Converted No-show Column  
- Yes → 1  
- No → 0  
- Makes the column numeric for analysis.

### 7️⃣ Corrected Wrong Column Names  
- Hipertension → hypertension  
- Handcap → handicap  
- No-show → no_show  
- Renamed all columns to lowercase with underscores.

### 8️⃣ Checked & Handled Missing Values  
- Used Conditional Formatting → Highlight Blanks  
- No major missing values found.

---

## ✅ Final Cleaned Columns

## 🛠 Tools Used  
- Microsoft Excel  
- Excel Formulas  
- Conditional Formatting  
- Excel Data Cleaning Tools  

---

## 📊 Summary  
Successfully cleaned the Medical Appointment dataset by:  
✔ Removing duplicates  
✔ Fixing invalid age values  
✔ Cleaning date formats  
✔ Standardizing gender & no-show  
✔ Adding new analytical column  
✔ Ensuring fully consistent column names  

Dataset is ready for EDA and modeling.

---

## 👨‍💻 Prepared By  
**Abhishek Singh**  
Data Analytics Intern
