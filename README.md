# Critical Slowing Down in Wealth Thermalization Phase Transition

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)

Official code repository for the 2026 paper: **"Early-Warning Signals of Critical Slowing Down in Wealth Thermalization Phase Transition: Theory, Quantification, and an Operational Dashboard."** This repository contains the core econometric scripts, numerical simulations, and data preprocessing pipelines used to establish the micro-macro bridge and empirically validate the five-dimensional early-warning matrix for wealth condensation across 40 economies.

## Framework Context
This work is the quantitative extension of the broader **"Verbs Persist"** theoretical framework. It applies Dissipative Structure Theory to global wealth distribution, proving that as economies approach the geometric singularity of CRJ = 12.0 (Empirical: 12.19) and absolute abundance epsilon_0 = 0.5, the system experiences severe **Critical Slowing Down (CSD)**. This is characterized by a diverging recovery half-life (tau), AR(1) coefficients (rho) approaching 1, and significant "flickering" in rolling variance.

## Repository Structure

* data/ 
  * 40_countries_2024_wealth_data.csv - The 2024 cross-sectional anchor data for 40 countries (derived from WID 2026).
* scripts/ 
  * 01_monte_carlo_langevin.py - (Appendix A) Langevin dynamics & Kramers barrier escape simulation.
  * 02_panel_unit_root_test.py - (Appendix B) Fisher-Type ADF stationarity tests validating I(0) for CSD indicators.
  * 03_csd_robustness_check.py - (Appendix C) 10/12/15/18-Year rolling window stress testing for absolute structural invariance.
  * 04_hansen_threshold_search.py - (Appendix D) Endogenous grid search algorithm isolating the 12.19 physical singularity and the 6.23x vulnerability multiplier.

## Quick Start & Reproducibility

Researchers can reproduce the diagnostic tests and theoretical simulations without complex environment configurations.

1. Clone the repository:
   git clone https://github.com/wealth-dynamics-lab/wealth-thermalization-csd.git
   cd wealth-thermalization-csd

2. Install standard dependencies:
   pip install numpy pandas matplotlib scipy statsmodels

3. Run the core Hansen singularity search (Appendix D):
   python scripts/04_hansen_threshold_search.py

## Interactive Early-Warning Dashboard
To bridge the gap between theoretical econophysics and actionable macroeconomic policy, we have developed a browser-based policy intervention simulator. Users can directly adjust system conversion rates (eta), extraction coefficients (beta), and institutional friction (R) to observe dynamic phase transitions and Kramers escape probabilities.

Live Dashboard Deployment: https://wealth-dynamics-lab.github.io/dashboard/

## License
This project is licensed under the MIT License. Free for academic and institutional reproducibility.
