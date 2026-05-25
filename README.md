# Crowdfunding Dashboard Analytics Dataset

This repository contains aggregated historical data tables exported from the **Crowdfunding Dashboard**. Featuring detailed breakdowns of campaign trends across global geographies, product categories, success rates, and temporal metrics spanning **2009 to 2019**, this dataset is optimized for exploratory data analysis (EDA), trend identification, and business intelligence (BI) modeling.

## 📊 Dataset Structure & Contents

The dataset is divided into four focused CSV tables representing different metrics and core dimensions of historical crowdfunding campaigns:

### 1. 📍 Projects by Locations
* **Filename:** `Crowdfunding Dashboard.xlsx - No.of Projects by Locations.csv`
* **Description:** Tracks the volume of unique crowdfunding projects across global geopolitical hubs.
* **Core Features:** `Row Labels` (City/State/Country), `Count of id` (Total Launched Projects).
* **Dataset Scale:** Includes 20,900 unique global locations.
* **Key Visual Insight:** Heavily dominated by creative tech hubs such as Los Angeles, CA (18,596), New York, NY (14,150), and London, UK (11,468).

### 2. 🏷️ Projects by Category
* **Filename:** `Crowdfunding Dashboard.xlsx - No.of Projects by Category.csv`
* **Description:** Breaks down market volume across distinct design, media, tech, and artistic categories.
* **Core Features:** `Row Labels` (Project Category/Sub-category), `Distinct Count of id` (Unique Projects).
* **Dataset Scale:** 160 distinct operational categories.
* **Key Visual Insight:** The highest project volumes belong to Product Design (22,277), Tabletop Games (15,618), and Music (15,194).

### 3. 📅 Number of Projects by Date
* **Filename:** `Crowdfunding Dashboard.xlsx - Number of Projects by Date.csv`
* **Description:** Hierarchical time-series analysis logging crowdfunding platform adoption, growth cycles, and cyclical seasonality.
* **Core Features:** `Row Labels` (Yearly, Quarterly, and Monthly nesting strings), `Count of id` (Launch Volume).
* **Dataset Scale:** 80 granular date intervals spanning from initial platform emergence in 2009 through 2019. Peak historic performance occurred between 2014 and 2015.

### 4. 📈 Percentage of Successful Projects
* **Filename:** `Crowdfunding Dashboard.xlsx - Percentage of Successful Projec.csv`
* **Description:** Success performance metrics across niche project sectors. Useful for risk assessment and predictive analytics.
* **Core Features:** `Row Labels` (Project Category), `successful_project_rate` (Decimal representation of success percentage).
* **Dataset Scale:** 160 comparative category rates.
* **Key Visual Insight:** While product design has volume, specific sub-niches lead in conversion efficiency: Chiptune (76.3%), Residencies (74.0%), and Anthologies (70.1%) yield the highest historical success rates.

---

## 🎯 Primary Use Cases

* **BI Dashboard Prototyping:** Build interactive visual maps and drill-down metrics using Tableau, Microsoft Power BI, Looker Studio, or Excel.
* **Geospatial Hotspotting:** Use Python or R mapping libraries to plot geographic nodes where distinct niches successfully coordinate backing.
* **Seasonality Evaluation:** Uncover launch windows (months or quarters) correlating with surges or slowdowns in collective user engagement.
* **Risk & Probability Modeling:** Evaluate structural relationships between category selections and campaign viability metrics.

---

## 🛠️ Code Snippets & Quick Start

Get started querying this repository's data files instantly with these native code recipes.

### Python (Pandas)
```python
import pandas as pd

# Load the categorical success rate dataset
success_df = pd.read_csv('Crowdfunding Dashboard.xlsx - Percentage of Successful Projec.csv')

# View top 10 highest-performing categories
highest_success = success_df.sort_values(by='successful_project_rate', ascending=False)
print(highest_success.head(10))
