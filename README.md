# EDA-Intelligent-System


# 🚀 DataLens — AI-Powered EDA Dashboard

![Version](https://img.shields.io/badge/version-2.4.1-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-production_ready-brightgreen)

---

## 📊 Overview

**DataLens** is a production-ready, fully automated **Exploratory Data Analysis (EDA)** dashboard that transforms raw datasets into actionable insights.

With zero configuration, it performs:

* Intelligent data ingestion
* Automated cleaning
* Feature engineering
* Statistical analysis
* Insight generation

All inside a **fast, responsive, browser-based interface**.

---

## ✨ Features

### 🔄 Complete Data Pipeline

* Multi-format ingestion: CSV, Excel, JSON
* Smart type detection (numerical, categorical, datetime)
* Missing value imputation

  * Numerical → Median
  * Categorical → Mode
* Duplicate removal
* Outlier detection (IQR method) + capping (winsorization)

---

### 📈 EDA Visualizations

* Histograms with KDE overlays
* Scatter plots for correlation
* Categorical bar charts
* Correlation matrix visualization
* Outlier distribution plots

---

### 🤖 Intelligent Insights (No External AI APIs)

* Missing value analysis
* Outlier detection reports
* Correlation discovery
* Class imbalance detection
* Feature quality recommendations

---

### 🎨 Modern Interface

* Dark theme optimized for analysis
* Fully responsive (mobile + desktop)
* Real-time processing indicators
* Exportable insights (JSON)

---

## 🚀 Quick Start

### Installation

```bash
git clone https://github.com/your-repo/datalens-eda.git
cd datalens-eda
```

### Run

Simply open:

```bash
index.html
```

in any modern browser (Chrome, Firefox, Edge, Safari).

---

## 📌 Usage

1. **Launch** → Open `index.html`
2. **Upload** → Drag & drop dataset (CSV, Excel, JSON)
3. **Analyze** → Pipeline runs automatically
4. **Explore**:

   * Dataset summary
   * Cleaning report
   * Visualizations
   * Insights
5. **Export** → Download insights as JSON

---

## 📁 Supported File Formats

| Format | Extension       | Notes                 |
| ------ | --------------- | --------------------- |
| CSV    | `.csv`          | Auto header detection |
| Excel  | `.xlsx`, `.xls` | First sheet only      |
| JSON   | `.json`         | Array of objects      |

---

## 🧠 Pipeline Architecture

```
Ingestion → Cleaning → Feature Engineering → Analysis → Insights
```

### Detailed Flow

**1. Data Ingestion**

* Detect file format
* Sample rows for type inference

**2. Data Cleaning**

* Remove duplicates
* Handle missing values
* Detect & cap outliers (IQR method)

**3. Feature Engineering**

* Type classification
* Missing flags
* Outlier annotations

**4. EDA**

* Distribution analysis
* Correlation analysis
* Category analysis

**5. Insight Generation**

* Statistical pattern detection
* Anomaly identification
* Recommendations

---

## 📊 Output Explanation

### Summary Cards

* Rows (after cleaning)
* Columns (with type breakdown)
* Missing %
* Outliers detected

### Schema Table

* Column types
* Missing count
* Unique values
* Sample data

### Visualizations

* Histogram → distribution shape
* Scatter → relationships
* Bar chart → category frequency
* Correlation → feature relationships

---

## ⚙️ Core Algorithms

### Type Detection

```js
if (sample.every(isNumeric)) → "numerical"
else if (sample.every(isDate)) → "datetime"
else → "categorical"
```

### Outlier Detection (IQR)

```js
IQR = Q3 - Q1
lower = Q1 - 1.5 * IQR
upper = Q3 + 1.5 * IQR
```

### Missing Value Imputation

```js
numerical → median()
categorical → mode()
```

---

## 🔒 Privacy & Security

* 100% client-side processing
* No data leaves your browser
* No tracking or analytics
* Works offline after load

---

## ⚡ Performance

| Dataset Size | Load Time |
| ------------ | --------- |
| < 1K rows    | Instant   |
| 1K–10K       | 1–2 sec   |
| 10K–100K     | 2–4 sec   |
| >100K        | Sampled   |

---

## 📱 Browser Support

* Chrome 90+ ✅
* Firefox 88+ ✅
* Edge 90+ ✅
* Safari 14+ ✅
* Mobile browsers ✅

---

## 🎯 Use Cases

### 👨‍💻 Data Scientists

* Quick EDA before modeling
* Feature correlation discovery

### 📊 Analysts

* Automated reports
* Data validation

### 🎓 Students

* Learn EDA workflows
* Practice visualization

### 🧑‍💼 Business Users

* Data quality checks
* High-level insights

---

## 🔧 Customization

### Change Outlier Threshold

```js
// Change 1.5 to 2.0 for stricter detection
let lower = q1 - 1.5 * iqr;
```

### Change Imputation Strategy

```js
// Replace median with mean
let mean = nums.reduce((a,b)=>a+b,0)/nums.length;
```

---

## 📦 Project Structure

```
datalens-eda/
├── index.html
├── README.md
└── LICENSE
```

---

## 🐛 Troubleshooting

**No data showing**

* Check headers in CSV
* Ensure JSON is array format

**Slow performance**

* Large files (>100MB) may lag
* Use sampling

**Charts not loading**

* Check browser console
* Ensure Chart.js is loaded

---

## 🤝 Contributing

Contributions are welcome!

Ideas:

* Add Parquet / Arrow support
* Add statistical tests (ANOVA, Chi-square)
* Export PDF reports
* Custom dashboards

---

## 📜 License

MIT License — free to use and modify.

---

## 💡 Final Note

DataLens is designed for:

> ⚡ speed
> 🔒 privacy
> 📊 clarity

No setup. No backend. Just open and analyze.

---

## Author

**Tejas Kumar H**


