# Urban Land Use / Land Cover Classification using Sentinel-2 and Random Forest

## 📌 Project Overview
This project demonstrates an end-to-end **urban Land Use / Land Cover (LULC) classification workflow**
using **Sentinel-2 multispectral imagery** and a **Random Forest machine learning classifier**.

The objective is to map major urban land cover classes by integrating:
- GIS-based preprocessing (QGIS)
- Pixel-level feature extraction
- Supervised machine learning in Python

---

## 🗺️ Study Area
**Tiruchirappalli (Trichy), Tamil Nadu, India**  
Coordinate Reference System (CRS): **EPSG:32644 (WGS 84 / UTM Zone 44N)**

---

## 📊 Final LULC Map
![LULC Classification Map](outputs/lulc_rf_trichy_2025.png)

---

## 🛰️ Data Used

- **Satellite:** Sentinel-2 Level-2A (ESA)
- **Acquisition Date:** March 13, 2025
- **Spatial Resolution:** 10 m
- **Spectral Bands Used:**
  - B02 (Blue)
  - B03 (Green)
  - B04 (Red)
  - B08 (Near Infrared)

> Note: Raw Sentinel-2 data is not included in this repository due to file size limitations.

---

## ⚙️ Methodology

1. Sentinel-2 tiles were mosaicked, reprojected, and clipped to the study area using QGIS.
2. Training polygons representing major LULC classes were manually digitized.
3. Pixel-level spectral features were extracted from multispectral bands.
4. A **Random Forest classifier** was trained using Python (scikit-learn).
5. The trained model was applied to the full raster to generate a classified LULC map.
6. Final cartographic outputs were created using QGIS Print Layout.

---

## 🧰 Tools & Technologies

- **GIS:** QGIS (LTR)
- **Programming Language:** Python 3.x
- **Machine Learning:** Random Forest (scikit-learn)
- **Geospatial Libraries:** rasterio, geopandas, numpy, pandas
- **Visualization & Mapping:** QGIS Print Layout
- **Version Control:** GitHub


---

## 📈 Results

- Overall classification accuracy: **~83%**
- Vegetation and water classes showed high precision due to strong spectral separability.
- Some confusion was observed between built-up and barren land, which is expected at 10 m resolution.
- The final output is a georeferenced LULC map suitable for urban analysis and planning applications.





