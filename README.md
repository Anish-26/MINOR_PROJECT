# 🇮🇳 India — Literacy vs Sanitation Analysis

This project is an end-to-end data analysis and visualization pipeline that explores the relationship between **Literacy Rates** and access to **Basic Sanitation Coverage** across the states and union territories of India. It features statistical correlation analysis, an interactive geospatial choropleth map, and a modern web dashboard.

## 🚀 Features

- **Data Analysis & Correlation** — Conducts Pearson correlation and R² variance evaluation between state-level literacy and sanitation data.
- **Interactive Choropleth Maps** — A dynamic Folium-based map toggling between:
  - **Basic Sanitation (%)**
  - **Total Literacy (%)**
- **Data Visualizations** — Clean bar plots detailing the Top 10 and Bottom 10 performing states.
- **Web Dashboard** — A comprehensive, responsive HTML/CSS dashboard aggregating analysis findings, visual charts, the interactive map, and the official source report.

---

## 📁 Project Structure

```text
minor/
├── DATA/
│   ├── final_result.csv        # Merged literacy + sanitation data by State/UT
│   ├── lit.csv                 # Raw literacy data
│   ├── san.csv                 # Raw sanitation data
│   └── SDG6.csv                # Raw SDG 6 (Water & Sanitation) data
│
├── GEOJSON/
│   ├── india.geojson           # GeoJSON boundaries for Indian districts/states
│   └── map.ipynb               # Jupyter notebook that generates the interactive Folium map
│
├── analysis/
│   └── comparison.ipynb        # Data analysis notebook (generates correlation & charts)
│
├── WEBSITE1/                   # Main Web Dashboard
│   ├── index.html              # Responsive front-end aggregating all findings & interactive map
│   ├── styles.css              # Custom styling for the dashboard
│   ├── map.html                # Exported interactive Folium map 
│   ├── scatter.png             # Correlation scatter plot
│   ├── sanitation_top10.png    # Top performing states chart
│   ├── sanitation_bottom10.png # Lowest performing states chart
│   └── FR375.pdf               # Official data source document
│
└── README.md                   # This file
```

---

## 🛠️ Tech Stack

| Tool        | Purpose                                            |
|-------------|----------------------------------------------------|
| **Python 3**| Core programming and data processing language      |
| **Pandas**  | Data loading, cleaning, merging, and manipulation  |
| **GeoPandas**| State-level boundary mapping and geometry handling|
| **Matplotlib**| Generation of static charts and scatter plots    |
| **Folium**  | Interactive Leaflet.js map generation              |
| **Jupyter** | Notebook environment for analytical exploration    |
| **HTML/CSS**| Building the modern, responsive web dashboard      |

---

## 🚀 Getting Started

### Prerequisites

Ensure you have Python installed along with the essential data science libraries:

```bash
pip install pandas geopandas folium matplotlib jupyter
```

### Running the Analysis

1. **Extract and Clean Data**: Run the relevant notebooks to process the `.csv` files within `DATA/`.
2. **Generate Statistical Charts**: 
   ```bash
   cd analysis
   jupyter notebook comparison.ipynb
   ```
   *Run all cells to generate `scatter.png`, `sanitation_top10.png`, and `sanitation_bottom10.png`.*
   
3. **Generate the Interactive Map**: 
   ```bash
   cd ../GEOJSON
   jupyter notebook map.ipynb
   ```
   *Run all cells to export the choropleth map as `map.html`.*
   
4. **View the Dashboard**:
   Copy generated charts and `map.html` to the `WEBSITE1/` folder. Open `WEBSITE1/index.html` in any web browser to explore the fully aggregated interactive report!

---

## 📊 Key Findings

- Our statistical findings demonstrated a **moderately strong positive correlation (r = 0.67)**, indicating that higher literacy is associated with better sanitation access.
- **R² = 0.45**, meaning 45% of sanitation variances can be explained by literacy progression, with the rest relying on geographic and socioeconomic policy factors.
- **Southern States** historically index strongly across both basic development metrics.

---

## 📄 License & Status

Developed as an educational data visualization and analysis minor project. Data sourced via official government statistics & published reports mapping SDG 6 indicators.
