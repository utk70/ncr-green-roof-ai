<div align="center">
  <img src="logo.png" height="80" alt="NCR Green Roof AI Logo"/>
  <p><strong>Combating Urban Heat Islands with Satellite Intelligence & Machine Learning.</strong></p>

  [![Project Status](https://img.shields.io/badge/Status-Live-success?style=for-the-badge&color=2ea44f)](https://utk70.github.io/ncr-green-roof-ai/)
  [![Tech Stack](https://img.shields.io/badge/Tech-Python%20|%20GEE%20|%20Folium-blue?style=for-the-badge)](https://github.com/utk70/ncr-green-roof-ai)
  
  <br/>
  
  <a href="https://utk70.github.io/ncr-green-roof-ai/">
    <img src="https://img.shields.io/badge/🚀_View_Live_Dashboard-Click_Here-000000?style=for-the-badge&logo=google-earth&logoColor=white" height="35" />
  </a>
</div>

---

## 📖 Overview
The **Urban Heat Island (UHI)** effect causes cities to be significantly hotter than rural areas due to dense concrete infrastructure. While Green Roofs (vegetation on rooftops) are a proven solution, financial constraints make it impossible to retrofit every building.

**NCR Green Roof AI** is a data-driven prioritization tool that identifies the **"Critical 1%"** of buildings in the Delhi NCR region that contribute most to local heating. By targeting these high-impact structures, city planners can maximize the environmental ROI of green roof retrofitting.

**Study Areas:**
* 🏭 **Greater Noida** (Industrial Focus)
* 🏢 **Gurugram** (Commercial/Cyber City)
* 🏠 **South Delhi** (Dense Residential)

---

## ⚙️ How It Works (Methodology)

We analyzed over **385,000 building footprints** using a custom data pipeline:

1.  **Satellite Data Acquisition:**
    * **Landsat 8 (TIRS):** Extracted Land Surface Temperature (LST).
    * **Google Open Buildings:** Acquired vector footprints for every structure.
2.  **The AI Algorithm:**
    * We developed a **Weighted Scoring Model** to rank buildings based on two factors:
        * **Heat Impact (70%):** Relative surface temperature compared to neighbors.
        * **Scalability (30%):** Available roof surface area.
3.  **Visualization & Optimization:**
    * Generated high-resolution interactive maps using **Geometry Simplification** and **Regional Slicing** (splitting cities into North/Central/South) to ensure sub-second load times on the web.

### 🧮 The Ranking Formula

We used a weighted percentile ranking system to calculate the final priority score:

> **Priority Score = (Heat_Rank × 0.70) + (Area_Rank × 0.30)**

| Priority Tier | Criteria | Action |
| :--- | :--- | :--- |
| 🔴 **CRITICAL** | Top 1% Score | Immediate Retrofit Recommended |
| 🟠 **HIGH** | Top 10% Score | Strong Candidate for Cooling |
| 🟡 **MEDIUM** | Top 50% Score | Long-term Consideration |
| 🟢 **LOW** | Bottom 50% | Maintain Current Status |

---

## 📊 Key Findings

| Region | Buildings Analyzed | Avg Temp | Peak Temp | Critical Buildings |
| :--- | :--- | :--- | :--- | :--- |
| **Greater Noida** | 102,853 | 31.2°C | 38.7°C | **1,265** |
| **Gurugram** | 124,089 | 32.5°C | 38.5°C | **2,413** |
| **South Delhi** | 158,503 | 31.4°C | 35.8°C | **177** |

> **Insight:** Gurugram exhibited the most severe heat clusters due to large commercial rooftops, while South Delhi's dense residential layout resulted in lower individual criticality scores.

---

## 🛠️ Technology Stack

* **Core Logic:** Python (Pandas, NumPy)
* **Geospatial Processing:** Google Earth Engine (GEE) API, Geopandas
* **Machine Learning:** Scikit-Learn (Percentile Ranking & Stats)
* **Visualization:** Folium, Matplotlib, Leaflet.js
* **Deployment:** GitHub Pages

---

## 🚀 How to Run Locally

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/utk70/ncr-green-roof-ai.git](https://github.com/utk70/ncr-green-roof-ai.git)
    ```
2.  **Open the Dashboard:**
    * Navigate to the folder and open `index.html` in your browser.
3.  **View Maps:**
    * Maps are split into parts (e.g., `noida_part1.html`) for performance. Click the buttons on the dashboard to load specific zones.

---

## 👨‍💻 Author

**Utkarsh**
* **Student ID:** 25SCS1003002916
* **Course:** Introduction to AIML
* **Institute:** IILM University

---

*This project was built for the End-Term Project submission, demonstrating the application of AI/ML in Urban Sustainability.*
