# 📊 Superstore Exploratory Data Analysis

> Exploratory analysis of the Superstore dataset to uncover patterns in **Sales, Profit, Discounts, Category Performance, Regional Performance, and business trends**.

---

## 🎯 Objective

Analyze the dataset using statistical and visual exploration to identify **patterns, relationships, outliers, and actionable business insights**.

---

## 📂 Dataset Overview

| Metric | Value |
|---|---:|
| Records | **9,994** |
| Columns | **21** |
| Missing Values | **0** |
| Duplicate Rows | **0** |
| Period | **2014–2017** |

### Key Variables

`Sales` · `Profit` · `Quantity` · `Discount` · `Category` · `Sub-Category` · `Region` · `Segment` · `Order Date` · `Ship Date`

---

## 🛠️ Tools & Libraries

- 🐍 **Python**
- 🐼 **Pandas** — data manipulation and exploration
- 🔢 **NumPy** — numerical operations
- 📊 **Matplotlib** — visualization
- 🎨 **Seaborn** — statistical visualization
- 📓 **Jupyter Notebook** — analysis and documentation

---

## 🔄 Analysis Performed

- Dataset structure and statistical summary
- Categorical distribution analysis
- Sales & Profit distribution
- Outlier analysis
- Sales vs. Profit relationship
- Discount vs. Profit relationship
- Category performance
- Regional performance
- Correlation analysis
- Time-based trend exploration

### Data Preparation

- Converted **Order Date** and **Ship Date** to datetime
- Extracted **Year** and **Month**
- Calculated **Shipping Days**
- Verified missing values and duplicate records

---

## 📈 Key Insights

### 💰 Sales & Profit

- Sales is strongly **right-skewed**, with most transactions concentrated at lower values.
- Profit is highly right-skewed with a skewness of approximately **7.56**.
- Profit ranges from approximately **-$6,599 to $8,399**.
- High-value observations represent legitimate large-scale transactions rather than obvious data errors.

### 🔗 Correlation Findings

| Relationship | Correlation | Interpretation |
|---|---:|---|
| Sales ↔ Profit | **0.48** | Moderate positive |
| Sales ↔ Quantity | **0.20** | Weak positive |
| Quantity ↔ Profit | **0.07** | Nearly neutral |
| Discount ↔ Sales | **-0.03** | Negligible |
| Discount ↔ Profit | **-0.22** | Weak negative |

> **Key Insight:** Higher Sales generally support higher Profit, but strong revenue does **not automatically guarantee profitability**.

---

## 🏷️ Category Performance

| Category | Sales | Profit |
|---|---:|---:|
| **Technology** | ~$836K | ~$145K |
| **Furniture** | ~$742K | ~$18K |
| **Office Supplies** | ~$719K | ~$122K |

- 🖥️ **Technology** leads in both Sales and Profit.
- 📎 **Office Supplies** generates strong Profit relative to its Sales.
- 🪑 **Furniture** generates substantial Sales but disproportionately low Profit.

> ⚠️ **Furniture is the clearest category-level profitability concern.**

---

## 🌎 Regional Performance

| Region | Sales | Profit |
|---|---:|---:|
| **West** | ~$725K | ~$108K |
| **East** | ~$678K | ~$92K |
| **Central** | ~$501K | ~$40K |
| **South** | ~$392K | ~$47K |

- **West** is the strongest region in both Sales and Profit.
- **East** also shows strong overall performance.
- **Central** generates more Sales than South but lower Profit.
- **South** has the lowest Sales but slightly higher Profit than Central.

> ⚠️ **Central requires closer investigation due to its weaker profitability.**

---

## 💡 Business Recommendations

| Focus Area | Recommendation |
|---|---|
| 🪑 **Furniture** | Review discount thresholds, pricing, and product-level costs |
| 💸 **Discount Strategy** | Control excessive discounting to protect margins |
| 📍 **Central Region** | Investigate operational and cost factors affecting profitability |
| 📊 **Performance Tracking** | Evaluate Sales and Profit together |
| 📈 **Decision Making** | Balance revenue growth with profitability and margins |

> **Note:** Correlation indicates association, not causation. The relationship between Discount and Profit should be investigated further rather than treated as proof of direct causality.

---

## 📁 Project Structure

```text
Superstore-EDA/
├── Dataset/
│   └── superstore.csv
├── notebook/
│   └── superstore_eda.ipynb
├── Report/
│   └── EDA_Report.pdf
└── README.md
