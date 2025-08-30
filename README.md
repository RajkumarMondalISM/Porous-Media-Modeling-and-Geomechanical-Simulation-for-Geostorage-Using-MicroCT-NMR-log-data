# Porous Media Modeling and Geomechanical Simulation for Geostorage Using MicroCT, NMR, and Wireline Log Data

## Overview
This repository provides a complete workflow for characterizing, simulating, and evaluating geostorage capacity in subsurface formations, by integrating micro-CT scan images, NMR data, and wireline logs. This approach ensures high-fidelity modeling of pore structures, calibration of petrophysical properties, and advanced geomechanical simulations to identify optimal geostorage sites with high porosity and low pressure.

---

## Workflow Summary

### 1. MicroCT Image Processing & Binary Segmentation
- **Objective:** Extract precise pore geometry from micro-CT scans.
- **Method:** Apply advanced denoising and adaptive thresholding for binary segmentation (rock vs. pore).
- **Outcome:** Binary images representing pore space for further network extraction.

  <img width="1480" height="510" alt="image" src="https://github.com/user-attachments/assets/83e2f378-b2e4-452a-b190-bbdeda531a37" />

<img width="790" height="490" alt="image" src="https://github.com/user-attachments/assets/e8c66543-6bd9-4b50-a22f-7a7fa2437911" />



### 2. Pore Network Modeling: Maximal Ball Algorithm
- **Objective:** Reconstruct pore network topology and metrics.
- **Method:** Use the maximal ball algorithm for robust identification of pore bodies and throats, preserving connectivity and realistic geometry.
- **Outcome:** Quantitative pore network (nodes, throats, size, connectivity) for property computation.

<img width="1471" height="595" alt="image" src="https://github.com/user-attachments/assets/b3b5fa8b-257f-43c3-9249-b925bc713d35" />


### 3. Calibration with NMR Data
- **Objective:** Ensure accuracy of porosity and permeability estimates.
- **Method:** Calibrate simulated micro-CT-derived porosity and permeability with NMR T2 relaxation measurements. Apply empirical relationships (e.g., Kozeny-Carman type) to link NMR and CT/PNM data for permeability estimation.
- **Outcome:** Reliable porosity and permeability distributions, accounting for sub-resolution and interconnected pore space.

POROSITY AND PERMEABILITY FROM NMR DATA FOR AN EXAMPLE (USING AN EXAMPLE DATA):
<img width="790" height="489" alt="image" src="https://github.com/user-attachments/assets/5386972a-6a5e-4e13-b5a7-bdfd4a1e2b1c" />

<img width="1805" height="789" alt="image" src="https://github.com/user-attachments/assets/9b1ebb98-4aa0-43d5-bffb-321ab0f719d9" />



### 4. 1D Geomechanical Modeling (PP, SHmax, Shmin)
- **Objective:** Compute in-situ stresses and pore pressure along the well path.
- **Method:** Integrate wireline well logs (density, sonic, etc.) and laboratory data. Model vertical (Sv), maximum horizontal (SHmax), and minimum horizontal (Shmin) stresses using calibrated well log relationships and formation pressure analysis. Employ Eaton’s and Anderson’s faulting theory as needed.
- **Outcome:** 1D Mechanical Earth Model (MEM) detailing pore pressure and stress states across reservoir depth.

1D GM FOR AN ILLUSTRATION (USING AN EXAMPLE DATA):

<img width="765" height="989" alt="image" src="https://github.com/user-attachments/assets/62c15ab3-1cb4-45f2-8bd4-b731e72f6cf9" />


### 5. Coupled Flow & Geomechanical Simulation
- **Objective:** Predict fluid flow using geomechanical feedback, supporting geostorage site selection.
- **Method:** Use upscaled properties (from CT/NMR/PNM calibration) and geomechanical results to run coupled reservoir simulators (FEM/FVM). Predict pressure, stress, and permeability evolution during storage scenarios.
- **Outcome:** Maps of flow and stress distribution, showing zones where geomechanical risk (high stress) is low, porosity is high and pressure is low within the storage.

### 6. Geostorage Site Evaluation
- **Objective:** Identify optimal geostorage locations.
- **Method:** Analyze simulation outputs for zones with low stress (max stability/minimum risk), high porosity (max storage capacity), and sufficient permeability (good injectivity). Apply integrated selection criteria based on widely accepted frameworks for CO2 or energy storage (e.g., IEA, NETL, GCCM).
- **Outcome:** Hierarchical ranking of candidate sites for safe, sustainable subsurface storage.




