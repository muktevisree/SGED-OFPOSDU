[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.16787636.svg)](https://doi.org/10.5281/zenodo.16787636)

## OSDU Schema Alignment

This dataset aligns with publicly available OSDU Well-Known Schemas (WKS) and entities as follows:

- **WKS:master-data--Facility (confirm version)** → Facility_ID, Facility_Name, Facility_Type, Latitude, Longitude, Facility_Status
- **WKS:master-data--Asset** → Asset, Sector, Company (as applicable)
- **WKE:Measurement** → Emission_Value_tCO2e, Energy_Consumed_kWh, Flaring_Volume_Mscf, Methane_tons
- **WKE:ProductionData** → Production_Volume, Production_Unit
- *(Proposed)* **EnvironmentalData extension** → Scope_1_tCO2e, Scope_2_tCO2e, Scope_3_tCO2e

See `schema-mapping/OFP_OSDU_Mapping_v1.0.csv` for the detailed field-level mapping and notes.

---

## Novelty Statement

To the best of our knowledge (as of Aug 15, 2025), this is the first publicly available dataset explicitly mapped to both the
Open Footprint (OFP) emissions model and the Open Subsurface Data Universe (OSDU) schemas (Facility, Asset, Measurement).
Unlike generic synthetic datasets, this work ensures schema compliance, FAIR principles, and dual-standards interoperability,
enabling ESG reporting validation and operational–sustainability data integration.

---

## How to Use

- Load the CSV/JSON and validate fields against OFP and OSDU schema expectations (see mapping CSV).
- Use `Emission_Type`, `Scope_*_tCO2e`, `Activity_Type`, and activity metrics to test ESG pipelines.
- Join on Facility or Asset identifiers to integrate with OSDU master data graphs.

---

## License

This dataset and supporting files are released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.  
You are free to share and adapt with proper attribution. See the LICENSE file for details.

---

## 📘 Notebook Demo

A quick-start Jupyter notebook is available to explore and visualize the dataset.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/muktevisree/SGED-OFPOSDU/blob/main/notebooks/example.ipynb)

### Run Locally
```bash
pip install -r requirements.txt
jupyter notebook notebooks/example.ipynb
