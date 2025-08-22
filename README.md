# Refining Gridded Asset Exposure Estimates with Auxiliary Co-variates and Aggregated Supervision

## Key Features

Aggregated Supervision: Instead of trying to perfectly match every noisy grid cell, the model is trained to match the more reliable sum of values over larger, aggregated tiles. This is inspired by Multiple Instance Learning (MIR), a technique suited for problems where high-resolution labels are noisy but coarser aggregates are more trustworthy.

Auxiliary Co-variates: We leverage globally available, high-resolution datasets for nighttime light intensity (Lit) and population count (Pop) to guide the model's predictions and reduce its dependence on the GEM data.

Uncertainty-Aware Predictions: Our framework explicitly quantifies the uncertainty of each prediction, providing a probabilistic interpretation of the re-estimated asset values. This helps users understand the reliability of the output and where caution is needed.

Robustness to Noise: The model's design includes a GEM sensitivity penalty that discourages it from becoming overly sensitive to the GEM input channel. This makes the predictions more stable in the presence of local GEM noise or estimation errors.


## data source
NIghttime light data : https://ladsweb.modaps.eosdis.nasa.gov/missions-and-measurements/products/VNP46A4/

Population : https://www.earthdata.nasa.gov/data/catalog/sedac-ciesin-sedac-gpwv4-popdens-r11-4.11

Asset exposure: https://www.globalquakemodel.org/product/global-exposure-model. 

Note that while GEM’s aggregated exposure data is freely available at the first administrative (Ad-
min 1) level, the dense high-resolution dataset used in this study is provided exclusively through
academic collaboration with GEM and is not publicly accessible.

## Repository Contents

Final_report.pdf: The full project report detailing the methodology, experiments, and results.

src/: Directory containing the source code, including the deep learning model architecture and training scripts.

data/: Placeholder for data files. The high-resolution GEM data used in this project is not publicly accessible due to academic collaboration agreements.


## Acknowledgments
I would like to thank Professor Ralf Toumi supervision and assessment of this project. I also acknowledge the Global Earthquake Model (GEM) Foundation for providing the high-resolution dataset for academic use.

This project was completed as part of the Machine Learning fand Big Data in the Physical science (MLBD) MRes program at Imperial College London.
