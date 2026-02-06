# Data Description

This folder contains all datasets used for the GIS-based analysis of playground availability across Berlin districts. The data were collected from open and official sources and processed using QGIS to assess spatial inequality in access to playgrounds relative to child population.

## Data Sources

### 1. OpenStreetMap Playground Data
**Source:** Geofabrik (OpenStreetMap)  
**Link:** https://download.geofabrik.de/europe/germany/berlin.html  

**Description:**  
This dataset contains point features representing public playground locations across Berlin. The data were extracted from OpenStreetMap via Geofabrik.

**Processing steps:**
- Filtered playground-related features from OSM data  
- Converted to point layer  
- Checked coordinate reference system (CRS) consistency  
- Used for spatial overlay and visualization of playground distribution  

### 2. Berlin District Boundaries (Bezirke)
**Source:** Open Data Informationsstelle Berlin (ODIS Berlin)  
**Link:** https://daten.odis-berlin.de/de/dataset/bezirksgrenzen  

**Description:**  
Polygon shapefile defining administrative boundaries of Berlin districts (Bezirke).

**Processing steps:**
- Loaded district boundary polygons into QGIS  
- Used as the spatial unit of analysis  
- Joined with playground counts and population data  

### 3. Population Statistics (Children aged 0–14)
**Source:** Statistik Berlin-Brandenburg  
**Link:** https://www.statistik-berlin-brandenburg.de/bevoelkerung/demografie/bevoelkerungsstand  

**Description:**  
Official demographic statistics providing the number of children aged 0–14 for each Berlin district.

**Processing steps:**
- Cleaned and formatted population tables  
- Joined population data to district boundaries  
- Used to calculate population-adjusted indicators  

## Derived Dataset

### Playground Availability Indicator
**File example:** `playground_per_1000_berlin.csv`

**Description:**  
A derived dataset created by combining playground counts and child population data.

**Indicator formula:**

                "𝐏𝐥𝐚𝐲𝐠𝐫𝐨𝐮𝐧𝐝𝐬 𝐩𝐞𝐫 𝟏,𝟎𝟎𝟎 𝐜𝐡𝐢𝐥𝐝𝐫𝐞𝐧"="Number of playgrounds" /"Child population (0–14)" ×1000

