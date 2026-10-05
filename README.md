# HR Analytics – Exploratory Data Analysis (EDA)

Exploratory analysis of a **2,000,000-record HR dataset** using Python, Pandas, NumPy, Matplotlib and Seaborn. The notebook validates and cleans the data, then explores workforce structure, compensation, experience, performance, employee status and work mode.

## 🎯 Objectives
- Validate and clean HR data (types, missing values, duplicates, ID and date consistency).
- Detect and treat salary outliers with the IQR method.
- Understand workforce distribution across departments, job titles, work modes and employee status.
- Study salary by department, job title and experience, and performance ratings by department.
- Examine correlations between numeric features and summarize the findings.

## 📂 Project structure
```
HR-Data-Analysis/
├── HR-Analysis.ipynb     # full analysis
├── requirements.txt
├── LICENSE
└── README.md
```
The dataset (`HR_Data_MNC_Data Science Lovers.csv`, ~180 MB) is **not included** in the repository because of its size. Download it and place it in the same folder as the notebook.

## 🧪 Notebook walkthrough
1. **Setup & loading** – imports, load the CSV, `info()` and `describe()`.
2. **Validation & cleaning** – drop the redundant index column, convert `Hire_Date` to datetime, check missing values and duplicate rows, **duplicate Employee_IDs**, **future hire dates**, experience-vs-tenure consistency, value-range and category checks.
3. **Outlier treatment** – IQR bounds on salary; outliers are capped (not deleted) and raw salary is kept in `Salary_Original`.
4. **Univariate analysis** – headcount by department, work mode, employee status, job-title headcount, **hires per year**.
5. **Bivariate analysis** – average salary by department and by job title, **salary vs. experience**, **performance rating by department**.
6. **Correlation analysis** – heatmap of the numeric features.
7. **Insights** – auto-generated findings, key takeaways and limitations.

## 📊 Visualizations (12)
Salary histogram · before/after salary boxplots · headcount by department · work-mode pie · employee-status pie · job-title headcount · hires per year · average salary by department · average salary by job title · salary vs. experience line chart · performance by department · correlation heatmap.

## 🔑 Key findings
- **IT is the largest department** (~30% of employees); the workforce is **60% On-site / 40% Remote** and **~70% Active**.
- **Job title, not experience, drives pay:** average salary stays flat (~INR 0.88M) from 0 to 15 years; IT Manager (~INR 1.67M) and Finance Manager (~INR 1.56M) are the highest-paid titles.
- **Performance is uniform:** every department averages ~3.0 / 5.
- ~3.5% of salaries were IQR outliers and were capped.
- The flat patterns and round percentages suggest the dataset is **synthetic**, so findings describe this dataset rather than real organisations.

## 🛠 Tools & technologies
Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook

## ▶️ How to run
```bash
git clone https://github.com/narmadha2006/HR-Data-Analysis.git
cd HR-Data-Analysis
pip install -r requirements.txt
# place "HR_Data_MNC_Data Science Lovers.csv" in this folder, then:
jupyter notebook HR-Analysis.ipynb
```
