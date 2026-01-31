# Acoustic Energy Harvesting: A Comparative Literature-Based Analysis

## Overview

This project presents a structured, exploratory analysis of **acoustic energy harvesting techniques** reported in the literature. Unlike experimental projects based on first-hand measurements, this study focuses on **secondary data extracted from peer-reviewed research articles**, with the goal of understanding:

- The **range of harvested power levels** reported across different approaches  
- The **operating frequency regimes** associated with each harvesting architecture  
- The **limitations of direct comparison** due to heterogeneous experimental conditions  

The work emphasizes **data curation, normalization-aware analysis, and honest interpretation**, rather than claiming definitive performance rankings.

---

## Motivation

Acoustic energy harvesting is often presented as a promising solution for powering low-energy devices using ambient sound. However, reported results vary widely across studies due to differences in:

- Sound pressure levels (SPL)
- Frequency content
- Harvester geometry and materials
- Power metrics (absolute power, power density, efficiency)

This project aims to **visually and conceptually organize these disparate results** to highlight trends, constraints, and gaps in the existing literature.

---

## Data Source and Scope

- All data used in this project were **manually extracted from published research papers** (MDPI, Springer, and related sources).
- No new experimental data were collected.
- Only **reported values** were used; no performance extrapolation was performed.

Each data entry includes:
- Harvesting approach and sub-approach  
- Reported harvested power and unit  
- Power type (absolute power, power density, efficiency, logarithmic units)  
- Sound pressure level (when available)  
- Operating frequency or frequency range (when available)  
- A qualitative **data comparability label**  

---

## Repository Structure

acoustic-energy-harvesting/
│
├── data/
│ └── acoustic_energy_harvesting_literature.csv
│
├── analysis/
│ └── AEH.ipynb
│
├── results/
│ └── acoustic_energy_harvesting.pdf
│
├── README.md
└── requirements.txt

---

## Methodology

### Data Curation
- Raw literature values were organized into a structured CSV format.
- Inconsistent reporting (ranges, efficiencies, power densities) was preserved rather than forced into uniform metrics.
- A `Data_Comparability` label was introduced to explicitly indicate whether values are:
  - **Comparable**
  - **Partially Comparable**
  - **Not Comparable**

### Analysis Approach
Using Python (pandas and matplotlib), the notebook explores:
- Distribution of reported harvested power by approach (log-scale)
- Relationship between harvested power and SPL (where available)
- Operating frequency ranges across harvesting architectures

No attempt is made to compute efficiencies or normalize across fundamentally incompatible metrics.

---

## Key Observations

- Resonator-based harvesters (Helmholtz, quarter-wavelength) operate in **narrow, low-frequency bands**.
- Acoustic metamaterial approaches span **broader frequency ranges**, suggesting greater adaptability.
- Standalone piezoelectric harvesting is typically reported at **higher frequencies**.
- Reported harvested power spans **multiple orders of magnitude**, even within the same approach.
- Direct performance comparison is often **not meaningful without standardized testing conditions**.

---

## Limitations

This study is intentionally exploratory and subject to several limitations:

- Data sourced from heterogeneous experimental setups
- Inconsistent reporting of SPL, frequency bandwidth, and loading conditions
- Presence of efficiency- and power-density-based metrics alongside absolute power
- No experimental validation or re-analysis of original signals

These limitations are explicitly acknowledged to avoid overinterpretation.

---

## Tools & Dependencies

- Python 3.x  
- pandas  
- matplotlib  
- Jupyter Notebook  

Install dependencies using:

```bash
pip install -r requirements.txt
