# RWA Data Layers & Metadata

If you find our work valuable, please consider giving us a star on GitHub!

![Repository](https://img.shields.io/badge/Repository-Metadata%20%26%20Methodology-blue)
![Standard](https://img.shields.io/badge/Standard-JSON%20%7C%20COG-orange)
![Storage](https://img.shields.io/badge/Storage-IPFS%20%7C%20GitHub-lightgrey)
![License](https://img.shields.io/badge/License-MIT%20%26%20CC--BY--4.0-green)

___

## Quick Start: How to Use and Verify This Data

This repository serves as a reference for verifiable RWA data. Here’s how you can interact with our work:

**1. Visually Explore the Asset:**
*   Go to the `boa_ventura_nr` folder.
*   Explore the `README.md` files within each data layer (e.g., `20231104_uav_dsm`) to understand the methodology.
*   Use the provided IPFS links to view the preview images of the Digital Surface Model and the VARI vegetation index.

**2. Cryptographically Verify the Data:**
*   **Choose a Data Layer:** For example, the high-resolution DSM (`ipfs://bafy...`).
*   **Download the Asset:** Download the full `.tif` file from IPFS.
*   **Calculate the Hash:** Use any standard tool to calculate the SHA-256 hash of the downloaded file.
*   **Verify:** Compare your calculated hash with the `hash_sha256` value recorded in the corresponding `metadata.json` file (also on IPFS). They must match exactly. This proves the data has not been tampered with.

**3. Contribute to the Methodology (Become a Collaborator):**
*   This is an open-source framework. If you are a GIS specialist, data scientist, or ReFi builder and have suggestions for improving our data processing or validation methods, we encourage you to:
    1.  **Open an Issue:** To start a discussion.
    2.  **Submit a Pull Request:** To propose a concrete improvement to our documentation or metadata structure.

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

___

## Ecosystem Recognition

E-co.lab is a recognized participant in the **[Avalanche Retro9000](https://retro9000.avax.network/)** program, a retroactive public goods funding initiative by the Avalanche Foundation. Our project has been approved for the "L1s & Infrastructure Tooling" round and is currently live for community voting by participants in the Avalanche ecosystem.

You can view our official submission and support our mission here: **[E-co.lab on Retro9000](https://retro9000.avax.network/discover-builders/cmebmfjtw02g5103tb8aalzvi)**

---

### Contributing

We believe in the power of open-source collaboration to build a more regenerative future. If you have suggestions for improving our methodologies or find any issues, please feel free to open an issue or submit a pull request.

---

### License

The documentation and code within this repository are licensed under the **MIT License**.

The data assets themselves (e.g., `.tif`, `.png` files linked via IPFS) and their corresponding metadata (`.json` files) are licensed under the **Creative Commons Attribution 4.0 International (CC-BY 4.0)**, allowing for re-use with proper attribution.