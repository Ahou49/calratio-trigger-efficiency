# Calratio Trigger Efficiency Analysis 
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
## Note on data
The ROOT input files used in this analysis are not included in this 
repository as they are part of the ATLAS collaboration internal dataset. The code is provided for reference purposes only.
## Dependencies
pip install uproot awkward pandas matplotlib numpy

# Configuration files

The `configs/` folder contains the YAML configuration files used to generate 
the ROOT ntuples with TopCPToolkit:

- `configs/particle.yaml` : particle level tree configuration
- `configs/reco.yaml`     : reconstruction level tree configuration

These files were used with the following command:

```bash
runTop_el.py -i local_inputs/ma15ctau100.txt -o ~/ntupleFW/outputFiles -p TopCalRatio/configs -t calRatio_merged -e 1000000 --no-systematics --particle | tee ~/ntupleFW/outputFiles/mc_output.log

```
