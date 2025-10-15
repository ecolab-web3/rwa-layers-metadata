# RWA Data Layer: Orthophoto

![Data Asset](https://img.shields.io/badge/Asset-Data%20Layer-green)
![Data Type](https://img.shields.io/badge/Type-Geospatial%20(Orthophoto)-blue)
![Software](https://img.shields.io/badge/Software-QGIS%20%7C%20GDAL-orange)
![License](https://img.shields.io/badge/License-CC--BY--4.0-lightgrey)

---

### Official E-co.lab Links

*   **Official Website:** [ecolab-web3.github.io](https://ecolab-web3.github.io)
*   **Whitepaper:** [e-co-lab.gitbook.io/whitepaper](https://e-co-lab.gitbook.io/whitepaper)
*   **Discord Community:** [discord.gg/mrSuw8AfjC](https://discord.gg/mrSuw8AfjC)
*   **Twitter:** [@ecolab_web3](https://twitter.com/ecolab_web3)

---

### About The Project

This repository documents the methodology and provides access to the **Orthophoto** data layer for the **Boa Ventura Natural Reserve**.

This layer serves as the high-resolution **visual baseline** of the asset at a specific moment in time (November 4, 2023). It is the primary source data from which analytical layers, such as the VARI (Visible Atmospherically Resistant Index), are derived.

As a foundational layer of the reserve's Digital Twin, the orthophoto enables visual verification of on-ground conditions and establishes a verifiable data lineage for all subsequent analyses within our Regenerative Finance (ReFi) framework.

---

### 📂 Data Layer Access & Details

This section provides direct access to the final, verifiable data assets stored on IPFS.

*   **Data Asset:** Orthophoto (COG)
    *   **Description:** A Cloud Optimized GeoTIFF representing the high-resolution visual state of the property.
    *   **URI:** [`ipfs://bafybeifxv2daxgdklmgr5hldnr6ufelpw43ujaln2awi75corpxv2ek6k4`](https://aquamarine-delicate-narwhal-626.mypinata.cloud/ipfs/bafybeifxv2daxgdklmgr5hldnr6ufelpw43ujaln2awi75corpxv2ek6k4)

*   **Preview Image:** Compressed Orthophoto Visualization
    *   **Description:** A compressed PNG rendering of the orthophoto for quick visualization.
    *   **URI:** [`ipfs://bafybeidxge7pkfsdlglypdpzf7ox67sdd3krg5ltfr63q57zhn7qxa2bl4`](https://aquamarine-delicate-narwhal-626.mypinata.cloud/ipfs/bafybeidxge7pkfsdlglypdpzf7ox67sdd3krg5ltfr63q57zhn7qxa2bl4)

*   **Metadata File:** Technical Specifications
    *   **Description:** A JSON file containing all acquisition parameters, processing details, raster properties, and proofs of integrity.
    *   **URI:** [`ipfs://bafkreib7twjtzal3g5tnrmdu4chw6ekenchclxszapb3ikixwiphyb6jz4`](https://aquamarine-delicate-narwhal-626.mypinata.cloud/ipfs/bafkreib7twjtzal3g5tnrmdu4chw6ekenchclxszapb3ikixwiphyb6jz4)

> ### ⚠️ Note on Local vs. On-Chain Data
>
> The `.tif` file present in this GitHub repository is a **low-resolution preview version** of the official data asset, created via resampling and compression to comply with GitHub's file size limits.
>
> *   **The official, high-resolution data asset** for quantitative analysis is the Cloud Optimized GeoTIFF stored on IPFS, accessible via the URI above.
> *   The `hash_sha256` documented in the metadata file **refers exclusively to the high-resolution file on IPFS**, ensuring the integrity and verifiability of the true on-chain asset.

---

### Processing Environment & Software

This project was developed using open-source GIS software to ensure quality and reproducibility.

*   **Primary Software:** QGIS `3.40.11-Bratislava`
*   **Core Libraries:** GDAL (Geospatial Data Abstraction Library)
*   **Photogrammetry Software:** WebODM
*   **Data Source:** `195` raw aerial images from a UAV survey on `2023-11-04`

---

### 💡 Key Concepts Implemented

*   **Data Lineage:** By documenting and registering the source orthophoto, we create a transparent and auditable "family tree" for all derived analytical products (like the VARI layer), strengthening the scientific rigor of the project.
*   **Data Integrity:** The final data asset is linked to a `SHA-256` hash recorded within the metadata JSON. This allows any third party to cryptographically verify that the data has not been altered since its registration.
*   **Web3 Optimization (COG):** The raw, multi-gigabyte GeoTIFF was converted into a Cloud Optimized GeoTIFF (COG). This industry-standard format ensures that applications can efficiently stream and access portions of the large image via IPFS without needing to download the entire file.
*   **Structured Metadata:** All acquisition and technical parameters, from the drone model and sensor type to the per-band color statistics, are documented in a standardized JSON file. This makes the data layer machine-readable and easy to integrate into automated workflows.

---

### Next Steps

*   **Develop Carbon & Biomass Layers:** Use the validated DSM and VARI layers as primary inputs for advanced modeling to estimate total biomass and sequestered carbon.
*   **Create a Water Body Data Layer:** Generate a specific layer delineating the property's water resources to enable the future issuance of water credits.
*   **On-Chain Integration:** Develop smart contracts to read and interpret these data layers for various ReFi applications.

---

### License

This repository and its documentation are licensed under the MIT License. The data assets themselves (`.tif`, `.png`) are licensed under the **Creative Commons Attribution 4.0 International (CC-BY 4.0)**.