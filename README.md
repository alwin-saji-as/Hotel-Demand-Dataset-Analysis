# 🏨 Hotel Demand Dataset Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat&logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualisation-11557c?style=flat)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualisation-4c72b0?style=flat)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)

---

## 📌 Project Overview

This project performs an end-to-end **Exploratory Data Analysis (EDA)** on real hotel booking data from two hotels in Portugal — a City Hotel and a Resort Hotel. The analysis uncovers patterns in cancellations, seasonal pricing, customer behaviour, and booking channels, generating actionable business insights for hotel revenue management.

---

## 📂 Repository Structure

Hotel-Demand-Dataset-Analysis/

│

├── Data/

│   └── hotels.csv

│

├── Notebook/

│   └── hotel_booking_analysis.ipynb

│

├── Visuals/

│   └── (12 chart images)

│

└── README.md


---

## 📊 Dataset

| Detail | Info |
|---|---|
| **Source** | Data in Brief — Antonio, Almeida & Nunes (2019) |
| **DOI** | https://doi.org/10.1016/j.dib.2018.11.126 |
| **Accessed via** | TidyTuesday GitHub Repository (https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2020/2020-02-11/hotels.csv) |
| **Hotels** | City Hotel & Resort Hotel, Portugal |
| **Period** | July 2015 — August 2017 |
| **Raw size** | 119,390 rows × 32 columns |
| **After cleaning** | 87,382 rows × 35 columns |

---

## 🔍 Steps Followed

### 1. Data Loading & Initial Overview
- Loaded dataset using Pandas
- Inspected shape, data types, and statistical summaries using `head()`, `info()`, and `describe()`

### 2. Data Pre-processing
- Dropped `company` column (94.31% missing)
- Handled missing values in `agent`, `country`, and `children`
- Removed 31,994 duplicate rows
- Fixed data types — datetime conversion, ordered categorical months
- Removed invalid ADR values (negative and extreme outliers)
- Recoded `Undefined` meal categories
- Created 4 derived columns: `total_nights`, `revenue`, `room_match`, `season`

### 3. Exploratory Data Analysis
- Univariate, bivariate, and multivariate analysis
- `groupby`, pivot tables, and correlation matrix
- Statistical summaries across cancellations, pricing, and demand

### 4. Visualisations
- 12 visualisations using Matplotlib and Seaborn
- Chart types: bar, histogram, box plot, line, grouped bar, heatmap
- All charts include titles, axis labels, legends, and annotations

### 5. Insights & Recommendations
- 5 key business insights derived from the analysis
- Actionable recommendations for hotel revenue management

---

## 📈 Sample Visualisations

### Distribution of Average Daily Rate (ADR)
![ADR Distribution](Visuals/2.%20Distribution%20of%20Average%20Daily%20Rate%20(ADR).png)

### ADR Distribution by Hotel Type
![ADR by Hotel Type](Visuals/6.%20ADR%20Distribution%20by%20Hotel%20Type.png)

### Correlation Heatmap of Numerical Variables
![Correlation Heatmap](Visuals/12.%20Correlation%20Heatmap%20of%20Numerical%20Variables.png)

---

## 📊 All Visualisations

| # | Title | Type |
|---|---|---|
| 1 | Overall Cancellation Rate | Bar Chart |
| 2 | Distribution of Average Daily Rate (ADR) | Histogram |
| 3 | Distribution of Lead Time | Histogram |
| 4 | Total Bookings by Hotel Type | Count Plot |
| 5 | Cancellation Rate by Hotel Type | Bar Chart |
| 6 | ADR Distribution by Hotel Type | Box Plot |
| 7 | Cancellation Rate by Market Segment | Horizontal Bar Chart |
| 8 | Average ADR by Season | Bar Chart |
| 9 | Monthly Booking Trend | Line Chart |
| 10 | Average ADR by Hotel Type and Season | Grouped Bar Chart |
| 11 | Cancellation Rate by Hotel Type and Deposit Type | Heatmap |
| 12 | Correlation Heatmap of Numerical Variables | Heatmap |

## 💡 Key Insights

1. **27.49% cancellation rate** — more than one in four bookings never resulted in a stay
2. **City Hotel cancels more** — 30.0% vs Resort Hotel's 23.5%, driven by high Online TA bookings
3. **Summer commands premium pricing** — Average ADR of €137.28 vs €75.51 in Winter
4. **Online TA highest cancellation risk** — 35.4% cancellation rate vs 14.7% for Direct bookings
5. **Non-refundable deposit paradox** — Non Refund bookings show cancellation rates above 97% for City Hotel

---

## ✅ Conclusion

This project demonstrates how Python libraries such as Pandas, Matplotlib, and Seaborn can be used for real-world hospitality data analysis. Starting from a raw dataset with missing values, duplicates, and inconsistent data types, the analysis pipeline produced clean, structured data that revealed meaningful patterns in hotel booking behaviour.

The insights gained — particularly around cancellation drivers, seasonal pricing, and booking channel risk — have direct practical value for hotel revenue management. The analysis shows that data-driven decision making can help hotels reduce cancellation rates, optimise pricing strategies, and improve overall occupancy and revenue performance.

## 🛠️ Tools & Libraries

| Tool | Purpose |
|---|---|
| Python 3.x | Core programming language |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical operations |
| Matplotlib | Data visualisation |
| Seaborn | Statistical visualisation |
| Jupyter Notebook | Development environment |

---

## 🚀 How to Run

1. **Clone the repository**
```bash
git clone https://github.com/alwin-saji-as/Hotel-Demand-Dataset-Analysis.git
```

2. **Navigate to the project folder**
```bash
cd Hotel-Demand-Dataset-Analysis
```

3. **Install required libraries**
```bash
pip install pandas numpy matplotlib seaborn
```

4. **Open the notebook**
```bash
jupyter notebook notebooks/hotel_booking_analysis.ipynb
```

### 📖 Alternative Method

1. Open `notebooks/hotel_booking_analysis.ipynb` using Jupyter Notebook or VS Code
2. Run the notebook cells step by step to view data cleaning, analysis, and visualisations
3. Modify the code to explore additional insights if needed
---


## 📧 Contact

**Alwin Saji**  
GitHub: [@alwin-saji-as](https://github.com/alwin-saji-as)

---

*Dataset source: Antonio, N., Almeida, A., & Nunes, L. (2019). Hotel booking demand datasets. Data in Brief, 22, 41–49. https://doi.org/10.1016/j.dib.2018.11.126*
