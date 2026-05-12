# 🧹 DataPulse AI — Data Cleaning & Insight Engine

An AI-powered data cleaning and analysis tool that automatically detects issues in any CSV dataset, cleans it, and lets you query it in plain English. Like having a data scientist in your browser — no Python, no Pandas, no setup required.

---

## 🔍 What It Does

Upload any messy CSV and DataPulse AI will:

- **Detect** missing values, duplicates, outliers, formatting inconsistencies, and type errors
- **Score** your dataset with a 0–100 Data Quality Score
- **Clean** it automatically — fills nulls, removes duplicates, normalizes dates, standardizes casing
- **Visualize** column distributions with auto-generated charts
- **Answer** plain-English questions about your data using AI

---

## 🚀 Live Demo

👉 [**Try it live →**](https://yourusername.github.io/datapulse-ai)

**Quick start:** Hit "Messy Sales Data" to load a sample with nulls, duplicates, outliers, and format errors — then click Analyze.

---

## 📸 Features

| Feature | Description |
|---|---|
| 🔍 Issue Detection | Nulls, duplicates, outliers (3σ), date format mismatches, case inconsistencies |
| 📊 Quality Score | 0–100 score with breakdown of what's dragging it down |
| ✨ Auto-Cleaning | One-click cleaning with configurable options per issue type |
| 📈 Auto-Charts | Bar + doughnut charts generated per column type automatically |
| 📋 Column Stats | Min, max, mean, null count, unique values per column |
| 🤖 AI Q&A | Ask anything about your data in plain English |
| ⬇️ Export | Download data quality report as text |

---

## 🧠 How It Works

```
CSV Upload (drag & drop or file picker)
    ↓
Parsing (PapaParse — handles malformed CSVs)
    ↓
Issue Detection Engine
    ├── Null detection (empty, "N/A", "UNKNOWN", "null")
    ├── Duplicate row detection (exact hash match)
    ├── Statistical outlier detection (Z-score > 3σ)
    ├── Date format normalization (DD/MM/YYYY → YYYY-MM-DD)
    └── Text case inconsistency detection
    ↓
Data Quality Score (weighted penalty model)
    ↓
Cleaning Pipeline (configurable — select which fixes to apply)
    ↓
Auto-Visualization (Chart.js — bar for numeric, doughnut for categorical)
    ↓
AI Analyst (Claude AI) — natural language Q&A on your dataset
```

### Issue Detection Details

- **Missing values** — detects empty strings, `N/A`, `UNKNOWN`, `null`, `NaN`
- **Outliers** — flags values more than 3 standard deviations from column mean
- **Duplicates** — exact row hash comparison across all columns
- **Format issues** — date inconsistencies (`01/27/2024` vs `2024-01-27`)
- **Case inconsistencies** — mixed `Electronics` / `electronics` / `ELECTRONICS`

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| AI Engine | Claude AI (claude-sonnet-4) via Anthropic API |
| CSV Parsing | PapaParse 5.4 |
| Data Visualization | Chart.js 4.4 |
| Statistical Analysis | Vanilla JS (Z-score, mean, mode, frequency) |
| Frontend | HTML / CSS / JavaScript (zero dependencies) |
| Deployment | GitHub Pages |

---

## 📂 Project Structure

```
datapulse-ai/
├── index.html       # Full app — parser, analysis engine, UI, AI chat
└── README.md
```

---

## ⚙️ Run Locally

```bash
git clone https://github.com/yourusername/datapulse-ai
cd datapulse-ai
open index.html
```

No install. No server. Works offline except for the AI Q&A feature.

---

## 📊 Sample Datasets Included

Three built-in messy datasets to demo instantly:

- **Messy Sales Data** — mixed date formats, nulls, negative values, duplicates, outliers
- **Employee Records** — missing salaries, invalid ages (150), duplicate IDs, bad emails
- **Inventory Data** — negative stock values, missing prices, duplicate SKUs, mixed casing

---

## 🎯 Why I Built This

Data cleaning is one of the most time-consuming parts of any data science workflow — estimates put it at 60–80% of a data scientist's time. Existing tools require Python/R knowledge. DataPulse AI makes it accessible to anyone: just upload a CSV and get a clean dataset with a quality report in seconds.

This project demonstrates:
- Statistical data analysis (Z-score outlier detection, frequency analysis)
- Data mining and pattern detection across tabular datasets
- Applied NLP for natural language data querying
- Full-stack data pipeline: parse → analyze → clean → visualize → explain

---

## 📋 Example Output

```
File: messy_sales_data.csv
Rows: 14 | Columns: 8
Quality Score: 52/100 — Poor Quality

Issues Found:
  🔴 Missing values (nulls, N/A, UNKNOWN)  → 6 cells across 3 columns
  🟡 Duplicate rows detected               → 2 exact duplicates
  🔴 Statistical outliers (>3σ from mean)  → 1 outlier in Sales column
  🔵 Formatting inconsistencies            → Date format mixed (2024/01/17)

After Cleaning:
  Quality Score: 89/100 — Good Quality ✅
  Rows removed: 2 (duplicates)
  Nulls filled: 6 (mean imputation for numeric, mode for text)
```

---

## 🗺️ Roadmap

- [ ] Excel (.xlsx) file support
- [ ] Export cleaned CSV directly
- [ ] Column-level AI explanations ("Why is this column 40% null?")
- [ ] Data schema inference and type casting
- [ ] Multi-file join and merge support

---

## 👤 Author

**Harshith Pankaja Mahendra**
CS Student @ University of New Brunswick
[LinkedIn](https://www.linkedin.com/in/harshith-mahendra-b61aa02a1)

---

> Part of an AI portfolio — see also [CloudLens AI](https://github.com/yourusername/cloudlens-ai) · [PhishGuard AI](https://github.com/yourusername/phishguard-ai) · [NetWatch AI](https://github.com/yourusername/netwatch-ai)
