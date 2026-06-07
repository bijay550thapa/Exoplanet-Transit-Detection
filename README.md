# Exoplanet Transit Detection using Kepler Data
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)]()
[![Data](https://img.shields.io/badge/Data-NASA%20Kepler-green.svg)]()

> [View Notebook on Colab](https://colab.research.google.com/github/bijay550thapa/Exoplanet-Transit-Detection/blob/main/exoplanet_detection.ipynb)

Independent research project — archival Kepler photometry, BLS period search, and transit characterization

> This project analyses archival photometric observations from the Kepler Space Telescope of HAT-P-7 to detect and characterise the transiting exoplanet HAT-P-7 b using the Box Least Squares (BLS) algorithm.

## Overview

HAT-P-7 b is a well-studied hot Jupiter orbiting its host star every ~2.2 days. This project recovers the planetary signal from archival Kepler light curve data using standard exoplanet detection techniques.

## Results

| Parameter | Value |
|---|---|
| Orbital period | 2.2047 days |
| Transit phase | 0.2195 |
| Transit depth | 0.00657 |
| Planet type | Hot Jupiter |
| BLS periods tested | 5,000 |

## Methodology

1. Downloaded archival HAT-P-7 light curve data from the Kepler mission using `lightkurve`
2. Cleaned the data by removing NaN values and outliers
3. Applied the Box Least Squares (BLS) algorithm across 5,000 trial periods from 1–3 days
4. Recovered an orbital period of 2.2047 days, confirmed by a sharp peak in the BLS periodogram
5. Phase-folded the light curve at the best-fit period, revealing a clear transit dip
6. Estimated a transit depth of 0.00657, consistent with a hot Jupiter blocking about 0.66% of the stellar flux
7. Calculated the transit phase as 0.2195 from the folded light curve

## Tools and Libraries

Python · `lightkurve` · `numpy` · `matplotlib` · `astropy` (`BoxLeastSquares`)

## Repository Contents

- Jupyter notebook with full code and analysis
- README with summary of method and results

## About

This project was completed independently as part of self-directed preparation for graduate research in observational astronomy. All data is publicly available from the Kepler mission archive.
