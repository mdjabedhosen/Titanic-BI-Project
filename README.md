# 🚢 Titanic BI Project

**Author:** Md Jabed Hosen  
**Tool:** Python (Google Colab)  
**Dataset:** Titanic Dataset (`Titanic_Dataset.csv`)

---

## 📋 Project Overview

This project performs a **Business Intelligence (BI) analysis** on the famous Titanic dataset. It covers the full data science pipeline — from raw data ingestion to cleaning, statistical analysis, and visual storytelling.

The goal is to uncover meaningful patterns in passenger survival using Python's data analysis and visualization libraries.

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `Titanic_Project_Colab.ipynb` | Original Jupyter Notebook (Google Colab) |

---

## 📦 Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
```

---

## 🔧 Section 1 — Data Cleaning

- Loaded dataset from Google Drive (`Titanic_Dataset.csv`) — **1,309 rows × 14 columns**
- Handled missing values:
  - `age` → filled with mean (`29.937`)
  - `cabin` → filled with mode (`C25`)
  - `fare` → filled with median grouped by passenger class
  - `boat` → filled with `"NoBoat"`
  - `home.dest` → filled with `"Unknown"`
  - `body` column → **dropped** (too many nulls)
- Created new features:
  - `family_size` = `sibsp + parch + 1`
  - `is_alone` = 1 if traveling alone, else 0
  - `age_group` = Child / Teen / Young / Adult / Senior
  - `fare_outlier` = True if fare > 1,000

---

## 📊 Section 2 — Data Analysis

| Group | Metric | Value |
|-------|--------|-------|
| Overall | Survival Rate | **38.2%** |
| Class 1 | Survival Rate | **61.9%** |
| Class 2 | Survival Rate | **43.0%** |
| Class 3 | Survival Rate | **25.5%** |
| Female | Survival Rate | **72.7%** |
| Male | Survival Rate | **19.1%** |
| Children | Survival Rate | **57.4%** |
| Seniors | Survival Rate | **24.2%** |

**Key Correlation Findings:**
- Passenger class has the strongest negative correlation with survival (`-0.31`)
- Fare has a slight positive correlation with survival (`+0.08`)

---

## 📈 Section 3 — Data Visualization

1. **Survival Pie Chart** — Overall survival split (~38% survived)
2. **Survival by Passenger Class** — Bar chart showing class 1 had the highest survival rate
3. **Survival by Embarkation Port** — Cherbourg (C) passengers had the best survival odds
4. **Survival by Sex & Class** — Women in all classes survived at much higher rates than men

---

## 🔍 Key Insights

- **Women** and **children** were prioritized during evacuation ("women and children first")
- **1st class** passengers had a significantly higher chance of survival than 3rd class
- Passengers who **embarked from Cherbourg** had the best survival rates
- **Traveling alone** vs. with family showed interesting differences in survival

---

## 🚀 How to Run

1. Open [Google Colab](https://colab.research.google.com/)
2. Upload `IT_Md_Jabed_Hosen.txt.ipynb`
3. Mount your Google Drive and place `Titanic_Dataset.csv` at:  
   `MyDrive/Jamib/Titanic_Dataset.csv`
4. Run all cells

---

## 📄 License

This project is for educational purposes only.
