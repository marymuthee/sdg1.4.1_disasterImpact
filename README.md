# Access to Basic Services and Disaster Impact in Africa (2022)

This repository presents an interactive web-based cartographic visualization examining the spatial relationship between **access to basic services (SDG Indicator 1.4.1)** and **disaster impact severity** across African countries in 2022.

The work was developed as part of an **Advanced Cartography** assignment and demonstrates the integration of geospatial data processing, thematic cartography, and interactive web mapping using R and Leaflet.

---

## Web Map Access

The interactive web map is available at:

**https://rpubs.com/marymuthee/disasters_and_sdg1**

---

## Objective

The objective of this project is to explore whether disparities in access to basic services—such as water, sanitation, and energy—are associated with variations in the human impacts of disasters across Africa. The map provides a visual, exploratory tool to support comparative spatial analysis and geospatial storytelling aligned with the Sustainable Development Goals (SDGs).

---

## Cartographic Design and Methodology

### Thematic Layers

#### 1. Access to Basic Services (Choropleth Polygons)
- Represents **SDG Indicator 1.4.1**:  
  *Proportion of the population living in households with access to basic services (%)*.
- Visualized using country-level polygon geometries.
- Class intervals:
  - `< 40 %`
  - `40 – 60 %`
  - `60 – 80 %`
  - `> 80 %`
- A neutral grey colour scheme was selected to reduce visual bias.
- Countries with missing data are explicitly represented as **NA** to preserve data integrity.

#### 2. Disaster Impact (Proportional Symbols)
- Represents the **total number of people affected by disasters in 2022**.
- Visualized using proportional red circle markers.
- **Square-root scaling** was applied to symbol sizes to account for the highly skewed distribution of disaster impacts and to maintain visual interpretability.
- Disaster symbols are programmatically forced to remain above polygon layers to ensure consistent visibility during interaction.

---

### Interaction Design

The map includes the following interactive components:
- Feature-level popups displaying country-specific values for both indicators.
- Layer controls enabling users to toggle thematic layers independently.
- Multiple basemap options (light, dark, grayscale, satellite) to support different viewing contexts.
- Separate legends for polygon classes and proportional symbols.
- An introductory information panel describing the map’s purpose and usage.

---

## Data Sources

- **Access to Basic Services**  
  United Nations SDG Database  
  *SDG Indicator 1.4.1 – Proportion of population living in households with access to basic services*

- **Disaster Impact Data**  
  Disaster impact dataset aggregated at the national level  
  *Total number of people affected by disasters in 2022*

- **Administrative Boundaries**  
  Africa country boundaries (GeoJSON format)

All datasets were processed and harmonized in R prior to visualization.

---

## Tools and Technologies

- **R** (geospatial data processing and visualization)
  - `sf`
  - `dplyr`
  - `leaflet`
  - `htmlwidgets`
  - `scales`
- **Leaflet.js** (via R bindings) for interactive web mapping
- **GitHub Pages** for map hosting and dissemination

---

## Cartographic Considerations

Key cartographic decisions underpinning this work include:
- The use of **choropleth mapping** for structural, long-term indicators and **proportional symbols** for event-based impacts.
- Explicit treatment of missing data to avoid misleading interpretations.
- Use of perceptually balanced colour schemes and symbol scaling to enhance readability.
- Layer ordering and interaction handling to preserve thematic clarity during user interaction.

---

md
