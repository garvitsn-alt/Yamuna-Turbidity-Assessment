# Yamuna River Turbidity Assessment Using Sentinel-2 and Google Earth Engine

## Project Overview

This project analyzes turbidity patterns along the Delhi stretch of the Yamuna River using Sentinel-2 satellite imagery and Google Earth Engine (GEE).

The objective was to identify spatial variations in turbidity and detect potential hotspot stretches using the Normalized Difference Turbidity Index (NDTI).

---

## Study Area

The Delhi section of the Yamuna River was divided into five stretches:

* Upstream 1
* Upstream 2
* Middle
* Downstream 1
* Downstream 2

---

## Data Source

* Sentinel-2 Surface Reflectance Harmonized
* Platform: Google Earth Engine
* Spatial Resolution: 10 meters
* Analysis Period: January 2025 – December 2025

---

## Methodology

### 1. Satellite Data Acquisition

Sentinel-2 imagery was filtered using:

* Study area boundary
* 2025 date range
* Cloud cover < 20%

### 2. Image Processing

* Created annual median composite
* Clipped imagery to study area

### 3. Water Extraction

Water bodies were identified using NDWI:

NDWI = (Green - NIR) / (Green + NIR)

### 4. Turbidity Assessment

Turbidity was estimated using NDTI:

NDTI = (Red - Green) / (Red + Green)

Where:

* Red = Sentinel-2 Band 4
* Green = Sentinel-2 Band 3

### 5. Statistical Analysis

For each river stretch:

* Minimum NDTI
* Maximum NDTI
* Mean NDTI
* Median NDTI

were calculated.

### 6. Hotspot Detection

Pixels with elevated NDTI values were classified as potential turbidity hotspots.

---

## Results

| Stretch      | Mean NDTI | Max NDTI |
| ------------ | --------: | -------: |
| Upstream 1   |     0.001 |    0.082 |
| Upstream 2   |    -0.049 |    0.086 |
| Middle       |    -0.041 |    0.087 |
| Downstream 1 |    -0.011 |    0.111 |
| Downstream 2 |    -0.008 |    0.120 |

---

## Key Findings

* Average turbidity remained relatively stable across the Delhi Yamuna stretches.
* No strong river-wide increase in average turbidity was observed.
* Maximum NDTI values increased downstream.
* Localized turbidity hotspots were more prominent in downstream stretches.
* The highest hotspot was observed in Downstream 2 (Max NDTI = 0.120).

---

## Environmental Insights

This analysis demonstrates how satellite remote sensing can be used to:

* Monitor river conditions
* Identify turbidity hotspots
* Support environmental screening
* Prioritize field investigations
* Generate spatial environmental indicators

---

## Tools & Technologies

* Google Earth Engine (GEE)
* Sentinel-2 Satellite Imagery
* Remote Sensing
* GIS Analysis
* NDTI
* NDWI
* Environmental Data Analytics

---

## Repository Structure

```text
Yamuna-Turbidity-Assessment/
│
├── README.md
├── gee_script.js
│
├── images/
│   ├── true_color.png
│   ├── ndti_map.png
│   └── hotspot_map.png
    ├── ndti_map_2.png
│   └── hotspot_map_2.png

│
└── results/
    └── stretch_statistics.csv
```

## Future Improvements

* Seasonal turbidity analysis
* Multi-year trend analysis
* Integration of water quality datasets
* Overlay of drains, STPs and industrial zones
* Automated hotspot monitoring

---

## Author

Garvit Saini

M.Sc. Environmental Science | Data Analyst | Remote Sensing & GIS Enthusiast
