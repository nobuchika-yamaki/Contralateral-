# Contralateral-
Contralateral 
# Contralateral Sensorimotor Wiring — Simulation Code

This repository contains all code and datasets used in the study:

**“Geometric and Evolutionary Constraints Explain the Origin of Contralateral Sensorimotor Wiring.”**

The code fully reproduces:
- Stage 1: Minimal geometric reaction-time model  
- Stage 2: Evolutionary optimization of 2×2 sensorimotor mappings  
- Stage 3: Empirical latency scaling analysis using 19 fish species  

All scripts use **Python 3.12**.

---

## Repository Structure

stage1_geometry/
geometric_model.py
run_geometry.py
params_stage1.json
stage2_evolution/
evolve_mapping.py
fitness_functions.py
params_stage2.json
stage3_empirical/
empirical_dataset.csv
latency_scaling.py
params_stage3.json
figures/
fig_geometry.png
fig_evolution.png
fig_empirical.png
README.md


---

## 1. Stage 1 — Geometric Reaction-Time Model

Compute minimal reaction times for:
- contralateral mapping  
- ipsilateral mapping  
- double-cross mapping  

Run:
python stage1_geometry/run_geometry.py

Output:
- nondimensional optimal latency t* ≈ 1.6  
- latency curves  
- optional 2D/3D robustness tests  

---

## 2. Stage 2 — Evolutionary Optimization

Unbiased evolution of a 2×2 mapping matrix under:
- mutation
- selection
- reaction-time cost
- behavioral correctness constraints

Run:
python stage2_evolution/evolve_mapping.py

Output:
- convergence to contralateral mappings (>99%)
- weight trajectory plots  

---

## 3. Stage 3 — Empirical Validation

Predictive model:
t_pred = (L / v) * t_star

Dataset:
stage3_empirical/empirical_dataset.csv

Run:
python stage3_empirical/latency_scaling.py

Output:
- predicted latency bands  
- empirical fast-start latency overlay  
- classification: inside / below / above model band  

---

## Dependencies

numpy
scipy
matplotlib
pandas

Install:
pip install -r requirements.txt

---

## Reproducibility

All data used in the manuscript are included in this repository.  
The code is identical to the version that will be archived on **Zenodo** with a DOI after acceptance.

---

## Contact

Nobuchika Yamaki
