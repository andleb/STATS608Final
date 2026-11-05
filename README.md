# Bayesian Time Series Modeling for Mobile Health

Final project for STATS 608 at the University of Michigan, April 2024, by **Andrej Leban and Luke Francisco**.

[Presentation (PDF)](STATS608%20presentation.pdf) · [PowerPoint](STATS608%20presentation.pptx)

We study imputation and prediction of mobile health measurements using the WISDM Smartphone and Smartwatch Activity and Biometrics Dataset. The outcome is the accelerometer resultant, modeled with Bayesian AR(1), AR(2), and AR(3) models that include subject and activity effects.

The models use static covariates derived from low-activity measurements, including averages, peak summaries, activity duration, and distributional entropy. For imputation, they also use concurrent sensor measurements. Posterior inference uses Hamiltonian Monte Carlo with the No-U-Turn Sampler in PyMC. The presentation describes the models and compares their fit, imputation, and prediction results.

## Notebooks

- [EDA.ipynb](EDA.ipynb): data exploration and preprocessing.
- [features.ipynb](features.ipynb): construction of static covariates.
- `ar1_imputation.ipynb`, `ar2_imputation.ipynb`, and `ar3_imputation.ipynb`: imputation models of increasing autoregressive order.
- `ar1_prediction.ipynb`, `ar2_prediction.ipynb`, and `ar3_prediction.ipynb`: corresponding prediction models.
- The matching `*_test.ipynb` notebooks evaluate the models on held-out observations.
