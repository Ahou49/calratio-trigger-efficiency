# calratio Trigger Efficiency Analysis 
## About 
This repository contains the code I wrote during my M2 internship at LPCA (Laboratoire de Physique de Clermont Auvergne), Université Clermont 
Auvergne, 2026.

The goal was to measure the CalRatio trigger efficiency for long-lived 
particles decaying to top quark pairs, using Monte Carlo simulation with Run 3 conditions at the ATLAS experiment at the LHC.

## Supervisors
- Dr. Louie CORPE (LPCA)
- Dr.Marion MISSIO (LPCA)
## What's in this repository
**01_efficiency.ipynb**
This notebook computes the trigger efficiency as a function of pT, Lxy and Lz for the benchmark point (mH, mS) = (1000, 475) GeV with 
cτ = 6.04 m.
**02_investigation_dip.ipynb**
This notebook investigates an unexpected efficiency dip at Lxy ~ 2.5 m. I tested nine different hypotheses to try to understand where it comes from. This notebook uses functions from 01_efficiency.ipynb.
## Requirements
- Python 3.8+
- uproot
- awkward
- pandas
- matplotlib
- numpy
## How to run
pip install -r requirements.txt
Then open the notebooks in order:
1. 01_efficiency.ipynb
2. 02_investigation_dip.ipynb


