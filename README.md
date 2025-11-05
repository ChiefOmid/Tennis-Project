[**English**](README.md) | [**فارسی**](README_fa.md)
---
# **🎾Tennis Match Data Analysis (60 Days)**

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?logo=jupyter)

---

## 🏆 Overview
This project provides an in-depth analysis of **60 days of professional tennis matches** scraped from [SofaScore.com](https://www.sofascore.com).  
The raw data was **messy, unstructured, and spread across multiple parquet files** for each day.  
The goal was to **clean, merge, and analyze** these datasets to extract key performance insights about players and matches.

---

## 📂 Dataset Structure
Each day’s folder (e.g., `20240101`, `20240102`, …) contained six Parquet datasets:

- `raw_match_parquet`
- `raw_odds_parquet`
- `raw_point_by_point_parquet`
- `raw_statistics_parquet`
- `raw_tennis_power_parquet`
- `raw_votes_parquet`

The combined dataset covers detailed information about matches, odds, player stats, and voting behavior.

> **Note:** Only a small sample of the dataset is included in this repository for demonstration purposes due to size and scraping policy.

---

## 🧠 Analysis Workflow
1. **Data Loading:** Read all 6 parquet datasets for each day and combined them into unified DataFrames.  
2. **Data Cleaning:** Removed duplicates, fixed column mismatches, and aligned player IDs using regex and `difflib`.  
3. **Data Integration:** Merged datasets based on `match_id` and `date`.  
4. **Exploratory Analysis:** Used Pandas, NumPy, and Matplotlib for performance metrics and visual insights.  
5. **Insight Extraction:** Correlations between odds, serve performance, and final outcomes were computed.

---

## 📊 Key Insights
- 📈 **Serve efficiency** is the strongest predictor of match success.  
- 🎯 **Pre-match odds** predicted outcomes with ~82% accuracy.  
- 💪 Players with higher “tennis power” ratings showed consistent break-point performance.  
- ⏱️ Patterns revealed **performance peaks at specific times** of the day and tournament stages.

---

## 🧩 Project Structure

---

## ⚙️ How to Run
1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/tennis-60days-analysis.git
   cd tennis-60days-analysis
----------------------------------------
2.Create and activate a virtual environment
python -m venv venv
source venv/bin/activate      # macOS/Linux
venv\Scripts\activate         # Windows

----------------------------------------
3.Install dependencies

pip install -r requirements.txt
---------------------------------------
4.Run Jupyter Notebook
jupyter notebook notebooks/tennis-project.ipynb

