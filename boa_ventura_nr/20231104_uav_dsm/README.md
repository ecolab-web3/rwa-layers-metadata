# RWA Data Layer: Digital Surface Model (DSM)

If you find our work valuable, please consider giving us a star on GitHub!

![Data Asset](https://img.shields.io/badge/Asset-Data%20Layer-green)
![Data Type](https://img.shields.io/badge/Type-Geospatial%20(DSM)-blue)
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

This repository documents the methodology and provides access to the Digital Surface Model (DSM) data layer for the **Boa Ventura Natural Reserve**.

This data layer represents the foundational physical structure of the asset, providing high-resolution topographic information. It is the first building block of the reserve's Digital Twin, designed for integration into Regenerative Finance (ReFi) protocols and tokenization as a Real World Asset (RWA) on the blockchain.

---

### 📂 Data Layer Access & Details

This section provides direct access to the final, verifiable data assets stored on IPFS.

*   **Data Asset:** Digital Surface Model (COG)
    *   **Description:** A Cloud Optimized GeoTIFF representing the surface elevation, including vegetation and other features.
    *   **URI:** [`ipfs://bafybeicj2up32uj3ioepuddg75k5rg2zib3x5s25whv3lsjlczh2iqolwm`](https://aquamarine-delicate-narwhal-626.mypinata.cloud/ipfs/bafybeicj2up32uj3ioepuddg75k5rg2zib3x5s25whv3lsjlczh2iqolwm)

*   **Preview Image:** Hillshade Visualization
    *   **Description:** A visual rendering of the DSM that highlights topographic features.
    *   **URI:** [`ipfs://bafybeihuufj6qq7liubcue7dxvfjy4ersqh3bhmltphub6x4by44g734f4`](https://aquamarine-delicate-narwhal-626.mypinata.cloud/ipfs/bafybeihuufj6qq7liubcue7dxvfjy4ersqh3bhmltphub6x4by44g734f4)

*   **Metadata File:** Technical Specifications
    *   **Description:** A JSON file containing all processing details, statistical summaries, and proofs of integrity.
    *   **URI:** [`ipfs://bafkreifgpgboyn4ffyeam7bhie4u2khp33my5wrrhcrlbmvca35chncgea`](https://aquamarine-delicate-narwhal-626.mypinata.cloud/ipfs/bafkreifgpgboyn4ffyeam7bhie4u2khp33my5wrrhcrlbmvca35chncgea)


> ### ⚠️ Note on Local vs. On-Chain Data
>
> The `.tif` file present in this GitHub repository is a **low-resolution preview version** of the official data asset, downsampled to comply with GitHub's file size limits.
>
> *   **The official, high-resolution data asset** for quantitative analysis is the Cloud Optimized GeoTIFF stored on IPFS, accessible via the URI above.
> *   The `hash_sha256` documented in the metadata file **refers exclusively to the high-resolution file on IPFS**, ensuring the integrity and verifiability of the true on-chain asset.

---

### Processing Environment & Software

This project was developed using open-source GIS software to ensure quality and reproducibility.

*   **Primary Software:** QGIS `3.40.11-Bratislava`
*   **Core Libraries:** GDAL (Geospatial Data Abstraction Library)
*   **Data Source:** Aerial survey with UAV on `2023-11-04`

---

### 💡 Key Concepts Implemented

*   **Data Integrity:** The final data asset is linked to a `SHA-256` hash (`D1A65...B74BB`) recorded within the metadata JSON. This allows any third party to cryptographically verify that the data has not been altered.
*   **Web3 Optimization (COG):** The raw GeoTIFF was converted into a Cloud Optimized GeoTIFF (COG). This ensures that applications can efficiently stream and access portions of the data via IPFS without needing to download the entire large file.
*   **Structured Metadata:** All technical properties and statistical analyses are documented in a standardized JSON file, making the data layer machine-readable and easy to integrate into smart contracts or other automated systems.

---

### Next Steps

*   **Develop Carbon & Biomass Layers:** Use the validated DSM and VARI layers as primary inputs for advanced modeling to estimate total biomass and sequestered carbon.
*   **Create a Water Body Data Layer:** Generate a specific layer delineating the property's water resources to enable the future issuance of water credits.
*   **On-Chain Integration:** Develop smart contracts to read and interpret these data layers for various ReFi applications.

---

## Ecosystem Recognition

E-co.lab is a recognized participant in the **[Avalanche Retro9000](https://retro9000.avax.network/)** program, a retroactive public goods funding initiative by the Avalanche Foundation. Our project has been approved for the "L1s & Infrastructure Tooling" round and is currently live for community voting by participants in the Avalanche ecosystem.

You can view our official submission and support our mission here: **[E-co.lab on Retro9000](https://retro9000.avax.network/discover-builders/cmebmfjtw02g5103tb8aalzvi)**

---

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

Please feel free to fork the repo and create a pull request, or open an issue with the tag "enhancement".

---

### License

This repository and its documentation are licensed under the MIT License. The data assets themselves (`.tif`, `.png`) are licensed under the **Creative Commons Attribution 4.0 International (CC-BY 4.0)**.