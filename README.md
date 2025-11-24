# ncr-green-roof-ai
# 🌱 NCR Green Roof AI

**Combating Urban Heat Islands with Satellite Intelligence & Machine Learning.**

[![Project Status](https://img.shields.io/badge/Status-Live-success)](https://utk70.github.io/ncr-green-roof-ai/)
[![Tech Stack](https://img.shields.io/badge/Tech-Python%20|%20GEE%20|%20Folium-blue)](#)

> **🚀 Live Dashboard:** [View the Interactive Maps](https://utk70.github.io/ncr-green-roof-ai/)

---

## 📖 Overview
The **Urban Heat Island (UHI)** effect causes cities to be significantly hotter than rural areas due to dense concrete infrastructure. Green roofs (vegetation on rooftops) are a proven solution, but they are expensive to implement universally.

**NCR Green Roof AI** is a data-driven prioritization tool that identifies the **"Critical 1%"** of buildings in the Delhi NCR region that contribute most to local heating. By targeting these high-impact structures, city planners can maximize the environmental ROI of green roof retrofitting.

**Study Areas:**
* 🏭 **Greater Noida** (Industrial Focus)
* 🏢 **Gurugram** (Commercial/Cyber City)
* 🏠 **South Delhi** (Dense Residential)

---

## ⚙️ How It Works (The Methodology)

We analyzed over **385,000 building footprints** using a custom data pipeline:

1.  **Satellite Data Acquisition:**
    * **Landsat 8 (TIRS):** Extracted Land Surface Temperature (LST).
    * **Google Open Buildings:** Acquired vector footprints for every structure.
2.  **The AI Algorithm:**
    * We developed a **Weighted Scoring Model** to rank buildings based on two factors:
    * **Heat Impact (70%):** How hot is the roof compared to neighbors?
    * **Scalability (30%):** How large is the available roof area?
3.  **Visualization:**
    * Generated high-resolution interactive maps using **Hybrid Geometry Optimization** (Polygons for critical buildings, Dots for low-priority ones) to ensure fast web performance.

### 🧮 The Ranking Formula
```math
Priority Score = (Heat Percentile \times 0.70) + (Area Percentile \times 0.30)

Priority Tier,Criteria,Action
🔴 CRITICAL,Top 1% Score,Immediate Retrofit Recommended
🟠 HIGH,Top 10% Score,Strong Candidate for Cooling
🟡 MEDIUM,Top 50% Score,Long-term Consideration
🟢 LOW,Bottom 50%,Maintain Current Status

Region,Buildings Analyzed,Avg Temp,Critical Buildings
Greater Noida,"102,853",31.2°C,"1,265"
Gurugram,"124,089",32.5°C,"2,413"
South Delhi,"158,503",31.4°C,177

🛠️ Technology Stack
Core Logic: Python (Pandas, NumPy)

Geospatial Processing: Google Earth Engine (GEE) API, Geopandas

Machine Learning: Scikit-Learn (Percentile Ranking & Stats)

Visualization: Folium, Matplotlib, Leaflet.js

Deployment: GitHub Pages
