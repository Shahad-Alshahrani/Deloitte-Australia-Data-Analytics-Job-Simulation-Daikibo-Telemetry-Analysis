# Deloitte Australia Data Analytics Job Simulation - Daikibo Telemetry Analysis

## 📌 Project Overview
This project is part of the **Deloitte Australia Data Analytics Virtual Internship** on Forage. The goal is to analyze telemetry data for a client, **Daikibo (Macora Industries)**, to identify manufacturing process bottlenecks and pinpoint the primary root causes of assembly line interruptions across global production facilities.

---

## 🎯 Business Problem
Daikibo collected one month of telemetry data (May 2021) in JSON format across 4 factories. Each factory contains 9 different machine types transmitting status messages every 10 minutes. The objective is to answer two core business questions:
1. 📍 **In which location did machines break down the most?**
2. 🛠️ **Which specific machines experienced the highest downtime in that location?**

---

## 📂 Dataset & Schema
* **Source File:** `daikibo-telemetry-data.json`
* **Coverage Period:** May 2021
* **Frequency:** 10-minute intervals per device
* **Locations:**
  * 🇯🇵 **Daikibo Factory Meiyo** (Tokyo, Japan)
  * 🇯🇵 **Daikibo Factory Seiko** (Osaka, Japan)
  * 🇩🇪 **Daikibo Berlin** (Berlin, Germany)
  * 🇨🇳 **Daikibo Shenzhen** (Shenzhen, China)

---

## ⚙️ Analysis & Implementation Steps (Tableau)

### 1. Data Preparation & Field Calculation
Imported the nested JSON telemetry dataset into Tableau, expanding all schema levels. Created a calculated field to measure total operational down time.

### 2. Visualization Components
📊 Down Time per Factory: Bar chart aggregated by location to highlight total downtime across all 4 plants.

🏭 Down Time per Device Type: Bar chart breakdown comparing downtime across all 9 machine categories.

🗺️ Down Time by Section & City: Heatmap illustrating downtime distribution across factory sections (section-1 to section-4) and cities.

### 3. Dashboard Interactivity
Built an interactive Tableau Dashboard integrating cross-filtering:

🖱️ Selecting a factory in the "Down Time per Factory" chart dynamically filters device types and factory sections to display localized breakdowns.

## 💡 Key Insights & Findings
* 🏭 Most Affected Location: Daikibo Factory Seiko (Osaka, Japan) registered the highest total downtime at 480 minutes, closely followed by Daikibo Shenzhen with 420 minutes.
* ⚡ Primary Bottleneck Machines: LaserWelder (480 mins) and LaserCutter (430 mins) accounted for the overwhelming majority of total equipment failures across facilities.
* 🔴 Operational Hotspots: Heatmap breakdown shows heavy downtime concentrated in specific assembly sections (e.g., section-4 in Osaka and section-3 in Shenzhen), indicating localized operational risks.

### 🛠️ Tools Used
* 📊 ['Tableau Desktop / Tableau Public (Data Modeling, Calculations, Dashboarding, Interactive Filtering)'](https://github.com/Shahad-Alshahrani/Deloitte-Australia-Data-Analytics-Job-Simulation-Daikibo-Telemetry-Analysis/blob/main/daikibo-telemetry-data.json.zip)
* 📄 JSON (Telemetry Data Source)
