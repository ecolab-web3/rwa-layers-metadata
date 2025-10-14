# RWA Data Layers & Metadata

![Repository](https://img.shields.io/badge/Repository-Metadata%20%26%20Methodology-blue)
![Standard](https://img.shields.io/badge/Standard-JSON%20%7C%20COG-orange)
![Storage](https://img.shields.io/badge/Storage-IPFS%20%7C%20GitHub-lightgrey)
![License](https://img.shields.io/badge/License-MIT%20%26%20CC--BY--4.0-green)

---

### Official E-co.lab Links

*   **Official Website:** [ecolab-web3.github.io](https://ecolab-web3.github.io)
*   **Whitepaper:** [e-co-lab.gitbook.io/whitepaper](https://e-co-lab.gitbook.io/whitepaper)
*   **Discord Community:** [discord.gg/mrSuw8AfjC](https://discord.gg/mrSuw8AfjC)
*   **Twitter:** [@ecolab_web3](https://twitter.com/ecolab_web3)

---

### About The Project

This repository serves as the central hub for the methodology, documentation, and metadata of all data layers associated with E-co.lab's Real World Assets (RWAs).

Our mission is to create a transparent, verifiable, and reproducible framework for bringing environmental assets on-chain. Each data layer represents a specific, measurable attribute of an RWA, forming the building blocks of a high-fidelity Digital Twin.

The first asset being documented here is the **Boa Ventura Natural Reserve**, a 2.1 million m² property targeted for the issuance of carbon, water, and biodiversity credits within the Regenerative Finance (ReFi) ecosystem.

---

### 🏛️ Repository Structure

This repository is organized hierarchically to ensure clarity and scalability as new assets and data layers are added.

```
rwa-layers-metadata/
│
└── <ASSET_NAME>/               (e.g., boa_ventura_nr)
    │
    └── <YYYYMMDD_SENSOR_DATATYPE>/ (e.g., 20231104_uav_dsm)
        │
        ├── README.md                 (Detailed methodology for this specific layer)
        ├── ..._metadata.json         (The machine-readable metadata file)
        └── ..._preview.tif           (A low-resolution preview of the data asset)
```

*   **`<ASSET_NAME>`:** A folder for each distinct Real World Asset.
*   **`<YYYYMMDD_SENSOR_DATATYPE>`:** A subfolder for each unique data acquisition event, identified by date, sensor, and the type of data generated (e.g., DSM, VARI).

---

### 💡 The RWA Data Layer Architecture

Our architecture is designed to provide a robust and decentralized "proof-of-reality" for on-chain assets, separating data storage from metadata and methodology.

1.  **On-Chain Asset (The Anchor of Trust):** An NFT (Non-Fungible Token) on the blockchain represents the legal or beneficial ownership of the RWA. Its primary role is to act as a secure, immutable pointer to the off-chain documentation that describes the asset.

2.  **Off-Chain Metadata & Methodology (This Repository):** GitHub serves as the layer for human-readable and machine-readable context.
    *   **`README.md`:** Provides a detailed, transparent, and reproducible account of the data collection and processing methodology. It is the "human-readable proof".
    *   **`metadata.json`:** A structured JSON file containing all technical specifications, statistical summaries, and cryptographic proofs (hashes) of the data. It is the "machine-readable proof".

3.  **Off-Chain Data Asset (The "What"):** Large geospatial files (e.g., Cloud Optimized GeoTIFFs) are stored on the **InterPlanetary File System (IPFS)**. This ensures decentralized, resilient, and content-addressed storage. The link between the metadata and the data is a cryptographic hash, ensuring that the metadata always points to the correct, unaltered data file.

---

### Key Concepts Implemented

*   **Verifiable Provenance:** We establish a dual-layer provenance system: cryptographic proof via SHA-256 hashes and IPFS CIDs, and methodological proof via the detailed documentation in this repository.
*   **Interoperability:** By using standardized formats like Cloud Optimized GeoTIFF (COG) and structured JSON, our data layers are designed to be easily consumed and integrated by third-party protocols, marketplaces, and analytical tools.
*   **Radical Transparency:** The entire process, from data acquisition to on-chain representation, is documented and made public to allow for full auditability by the community and stakeholders.
*   **Efficient Accessibility:** The use of COG on IPFS allows applications to efficiently stream only the necessary portions of large geospatial datasets, making the data usable in web environments without requiring full downloads.

---

### Contributing

We believe in the power of open-source collaboration to build a more regenerative future. If you have suggestions for improving our methodologies or find any issues, please feel free to open an issue or submit a pull request.

---

### License

The documentation and code within this repository are licensed under the **MIT License**.

The data assets themselves (e.g., `.tif`, `.png` files linked via IPFS) and their corresponding metadata (`.json` files) are licensed under the **Creative Commons Attribution 4.0 International (CC-BY 4.0)**, allowing for re-use with proper attribution.