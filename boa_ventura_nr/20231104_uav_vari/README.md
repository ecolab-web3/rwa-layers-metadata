# RWA Data Layer: Visible Atmospherically Resistant Index (VARI)

![Data Asset](https://img.shields.io/badge/Asset-Data%20Layer-green)
![Data Type](https://img.shields.io/badge/Type-Geospatial%20(VARI)-blue)
![Software](https://img.shields.io/badge/Software-QGIS%20%7C%20GRASS%20%7C%20GDAL-orange)
![License](https://img.shields.io/badge/License-CC--BY--4.0-lightgrey)

---

### Official E-co.lab Links

*   **Official Website:** [ecolab-web3.github.io](https://ecolab-web3.github.io)
*   **Whitepaper:** [e-co-lab.gitbook.io/whitepaper](https://e-co-lab.gitbook.io/whitepaper)
*   **Discord Community:** [discord.gg/mrSuw8AfjC](https://discord.gg/mrSuw8AfjC)
*   **Twitter:** [@ecolab_web3](https://twitter.com/ecolab_web3)

---

### About The Project

This repository documents the methodology and provides access to the Visible Atmospherically Resistant Index (VARI) data layer for the **Boa Ventura Natural Reserve**.

This layer quantifies the health and density of vegetation across the property, serving as a verifiable proxy for biomass and photosynthetic activity. It is a critical input for carbon credit methodologies, biodiversity assessments, and other Regenerative Finance (ReFi) applications built upon the RWA framework.

---

### 📂 Data Layer Access & Details

This section provides direct access to the final, verifiable data assets stored on IPFS.

*   **Data Asset:** Vegetation Index (COG)
    *   **Description:** A Cloud Optimized GeoTIFF representing vegetation health, derived from the VARI formula.
    *   **URI:** [`ipfs://bafybeicl4xafzxasbi7c4y7x4n22khqpyikrrccqzbu7aur6yb3crhmufa`](https://aquamarine-delicate-narwhal-626.mypinata.cloud/ipfs/bafybeicl4xafzxasbi7c4y7x4n22khqpyikrrccqzbu7aur6yb3crhmufa)

*   **Preview Image:** VARI Visualization
    *   **Description:** A visual rendering of the VARI layer using a greenness color ramp.
    *   **URI:** [`ipfs://bafybeihs4umqf6h5qpgf5uexsxbchkukdhp4hkr6sduy35crijjaskj6bu`](https://aquamarine-delicate-narwhal-626.mypinata.cloud/ipfs/bafybeihs4umqf6h5qpgf5uexsxbchkukdhp4hkr6sduy35crijjaskj6bu)

*   **Metadata File:** Technical Specifications
    *   **Description:** A JSON file containing all processing details, statistical summaries, and proofs of integrity.
    *   **URI:** `[INSERIR LINK IPFS DO VARI_METADATA.JSON AQUI]`

---

### Processing Environment & Software

This project was developed using open-source GIS software to ensure quality and reproducibility.

*   **Primary Software:** QGIS `3.40.11-Bratislava`
*   **Core Libraries:** GDAL, GRASS GIS (`r.neighbors`)
*   **Data Source:** Orthophoto from aerial survey with UAV on `2023-11-04`

---

### 🔬 Data Validation & Methodology

Equivalent to "Test Coverage" for smart contracts, this section outlines the rigorous process used to ensure the data's accuracy and reliability.

1.  **Data Cleaning:** Initial VARI calculation produced anomalous values (-21 to 24) due to sensor limitations in dark areas (water/shadow). The data was cleaned by "clamping" values to the scientifically accepted range of -1 to 1 using the GDAL Raster Calculator.
2.  **Spatial Smoothing:** The high resolution of the drone data introduced significant noise (the "salt-and-pepper" effect). A spatial smoothing filter (`r.neighbors`) was applied to generalize the data, ensuring that the classification reflects broader vegetation classes (fitofisionomias) rather than individual leaves or shadows.
3.  **Ground Truth & Iterative Classification:** The classification was refined through an iterative process, comparing the raster's histogram with ground-truth photos and visual analysis of the orthophoto. This ensured that the spectral signatures were correctly mapped to the real-world ecological classes of the Cerrado biome.
4.  **External Scientific Validation:** The final classification was cross-referenced with satellite data. The **NDVI** (the scientific standard index) was calculated from a Sentinel-2 image (10m resolution, ESA). A zonal statistics analysis confirmed a **strong positive correlation**, showing that our VARI-based classes align perfectly with the biomass progression measured by the satellite.

---

### 💡 Key Concepts Implemented

*   **Data Integrity:** The final COG is linked to a `SHA-256` hash (`4FE7B...B94DF`) within its metadata file, allowing for cryptographic verification of its authenticity.
*   **Ecological Accuracy:** The classification methodology goes beyond simple spectral analysis, incorporating ground-truthing and external validation to create a data layer that accurately reflects the unique characteristics of the Cerrado biome.
*   **Hierarchical Data Structure:** This VARI layer is designed to be geospatially aligned with the foundational DSM layer, allowing for future analyses that combine topographic and biological data (e.g., calculating biomass per hectare on sloped terrain).

---

### Next Steps

*   **Develop Carbon & Biomass Layers:** Use the validated DSM and VARI layers as primary inputs for advanced modeling to estimate total biomass and sequestered carbon.
*   **Create a Water Body Data Layer:** Generate a specific layer delineating the property's water resources to enable the future issuance of water credits.
*   **On-Chain Integration:** Develop smart contracts to read and interpret these data layers for various ReFi applications.

---

### License

This repository and its documentation are licensed under the MIT License. The data assets themselves (`.tif`, `.png`) are licensed under the **Creative Commons Attribution 4.0 International (CC-BY 4.0)**.