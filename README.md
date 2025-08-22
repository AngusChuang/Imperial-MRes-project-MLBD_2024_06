# Refining Gridded Asset Exposure Estimates with Auxiliary Co-variates and Aggregated Supervision

Quantifying asset exposure on the ground is a critical step in assessing the potential economic impact of natural disasters. While global datasets such as those provided by the Global Earthquake Model (GEM) Foundation offer valuable information on asset locations and values, these estimates are often uncertain at fine spatial scales. 

This project proposes a machine learning framework to improve the reliability of asset exposure estimates by learning from GEM data in combination with publicly available auxiliary sources, such as satellite-based nighttime light intensity and population count. By converting all inputs into a gridded spatial format and training the model on a reference region, the approach aims to reduce sensitivity to potentially unreliable inputs and produce more stable, uncertainty-aware asset predictions at a fine spatial resolution by leveraging external auxiliary co-variates.

To account for the challenges of noisy supervision and uncertain ground truth, the model is designed to learn patterns over aggregated spatial tiles, allowing it to capture robust signals while softening the influence of locally inconsistent data. Additionally, the framework includes a mechanism to quantify aleatoric uncertainty and control the level of trust placed in each data source during training.

Beyond its immediate relevance for disaster risk modelling, the methodology developed here contributes to broader efforts in geo-spatial machine learning, particularly in settings where reliable ground truth is limited and robustness to noisy inputs is essential.
