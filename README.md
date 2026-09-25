# M2 Globular Cluster — Isochrone Fitting (SDSS + MIST)

This repository contains Python code and analysis for fitting **MIST v1.2 stellar isochrones** to **SDSS photometric data** of the **M2 globular cluster (NGC 7089)**. The goal is to determine the best‑fit **age**, **metallicity**, and **distance** by comparing theoretical isochrones to the observed color–magnitude diagram (CMD).

## Overview

The workflow consists of three main steps:

1. **Age variation** — Compare isochrones of 12, 13, and 14 Gyr  
2. **Metallicity variation** — Compare isochrones with [Fe/H] from –1.75 to –1.55  
3. **Distance variation** — Test distances from 12 to 14.5 kpc  

SDSS photometry is queried using `astroquery.sdss`, and MIST isochrones are loaded using `read_mist_models`.

## Results

- **Best age:** 14 Gyr  
- **Best metallicity:** [Fe/H] = –1.55  
- **Best distance:** 13.5 kpc  

These parameters produce the isochrone that best traces the SDSS CMD of M2.

## Dependencies

- numpy  
- pandas  
- matplotlib  
- astropy  
- astroquery  
- read_mist_models  

## How to Run

1. Query SDSS data (or use the included CSV).  
2. Download MIST isochrones from the MIST web interface.  
3. Update file paths in the notebook.  
4. Run the Jupyter notebook to reproduce the analysis.

## Files

- `M2_SDSS_data.csv` — SDSS photometric catalog  
- `MIST_iso_*.iso.cmd` — MIST isochrone files  
- `MIST-Copy1.ipynb` — Main analysis notebook  

---

