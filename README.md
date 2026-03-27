## 🌬️ AirWatch BD: Intelligent Air Quality Monitoring

**High-Resolution Spatial Assessment of Atmospheric Pollutants & Public Health Vulnerability across Dhaka City using Google Earth Engine.**

[![Live Demo](https://img.shields.io/badge/Live_Dashboard-AirWatch_BD-00d4ff?style=for-the-badge&logo=google-earth)](https://your-username.github.io/AirWatch-BD/)
[![Powered by GEE](https://img.shields.io/badge/Google_Earth_Engine-Platform-333333?style=for-the-badge&logo=google)](https://earthengine.google.com/)

---

## 📌 Overview

**AirWatch BD** is an interactive, satellite-driven air quality monitoring system designed for Bangladesh. Utilizing Copernicus Sentinel-5P TROPOMI data, this application tracks 7 major atmospheric pollutants from 2020 to 2025. 

Beyond simple visualization, AirWatch BD features a dynamic **Vulnerability Assessment Model** that combines pollutant densities with socio-economic and environmental risk factors to generate localized public health advisories.

🔗 **[Launch the Interactive Dashboard](https://your-username.github.io/AirWatch-BD/)**

---

## ✨ Key Features

* **Multi-Pollutant Tracking:** Annual, monthly, and daily mean tracking for NO₂, SO₂, CO, O₃, HCHO, CH₄, and Aerosol Index (UVAI).
* **Dynamic Vulnerability Composite:** An 8-factor spatial composite layer highlighting highly susceptible population zones.
* **Automated Health Advisories:** Click anywhere on the map to query the normalized ratio of all pollutants and receive automated WHO-aligned health guidelines.
* **5-Year Trend Analysis:** Built-in charting for long-term air quality comparisons (2020–2025).
* **Correlation Heatmaps:** Interactive Pearson correlation matrix identifying relationships between pollutants, heat islands, and population density.

---

## ⚙️ Methodology: Vulnerability Assessment Model

The Vulnerability Layer is a weighted spatial composite. Each factor is normalized to a 0–1 scale and combined using the following weighting scheme to identify high-risk zones:

| Risk Factor | Source Dataset | Weight |
| :--- | :--- | :--- |
| **Nitrogen Dioxide (NO₂)** | Sentinel-5P TROPOMI | 20% |
| **Population Density** | WorldPop Global (100m) | 20% |
| **Land Surface Temp (LST)** | MOD11A1 (Heat Island Effect) | 15% |
| **Sulfur Dioxide (SO₂)** | Sentinel-5P TROPOMI | 10% |
| **Carbon Monoxide (CO)** | Sentinel-5P TROPOMI | 10% |
| **Aerosol Index (UVAI)** | Sentinel-5P TROPOMI | 10% |
| **Green-Space Deficit** | Inverse NDVI (MOD13A2) | 10% |
| **Methane (CH₄)** | Sentinel-5P TROPOMI | 5% |

---

## 📦 Data Provenance

All datasets utilized in this application are open-source and computationally processed via Google Earth Engine.

* **Atmospheric Data:** Copernicus Sentinel-5P OFFL L3 (European Space Agency)
* **Population:** WorldPop Global Project
* **Thermal & Vegetation:** NASA LP DAAC (MODIS Terra)
* **Administrative Boundaries:** FAO GAUL 2015 (Level 2 - Dhaka City)

---

## 📁 Repository Structure

```text
📦 AirWatch-BD
 ┣ 📜 README.md           # Project documentation
 ┣ 📜 index.html          # Web wrapper & landing page UI
 ┗ 📂 GEE_Scripts
   ┗ 📜 AirWatch_Main.js  # Core Google Earth Engine Application script Air-watch-BD
