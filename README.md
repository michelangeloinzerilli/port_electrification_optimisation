# Grid Impact Assessment and Energy Optimization of the Electrified Port of Oskarshamn

Master's Thesis developed at **KTH Royal Institute of Technology** in collaboration with **Oskarshamn Energi AB** and **Smålandshamnar AB**.

## Overview

This project investigates the impact of the planned electrification of the Ferry and Cargo Terminals at the Port of Oskarshamn, Sweden, on the local distribution grid.

The study integrates **electric port vehicles, Onshore Power Supply (OPS), photovoltaic generation (PV), and Battery Energy Storage Systems (BESS)** to evaluate how flexibility can reduce grid stress and electricity costs.

## Methodology

A four-stage lexicographic **Mixed-Integer Linear Programming (MILP)** model was developed in Python using **Pyomo** and **Gurobi** to optimize EV charging.

The resulting load profiles were integrated into a **pandapower** distribution-grid model to perform time-series power-flow simulations and assess line loading, transformer loading, and bus voltages under different electrification scenarios.

## Repository Structure

- **`CargoTerminal_coding/`** – EV charging optimization model for the Cargo Terminal.
- **`FerryTerminal_coding/`** – EV charging optimization model for the Ferry Terminal.
- **`inputs/`** – Input data provided by the collaborating companies or obtained from external sources.
- **`network data/`** – Network input data and processed outputs used in the grid simulations.
- **`network_CargoTerminal/`** – Power-flow simulations for the different Cargo Terminal scenarios.
- **`network_FerryTerminal/`** – Power-flow simulations for the different Ferry Terminal scenarios.

The subfolders within the two `network_*` directories contain the specific inputs used to evaluate each scenario. Depending on the scenario, modifications to the network model were introduced to account for the presence of the BESS and its dispatch objective.

PV generation and BESS dispatch profiles used as inputs for both terminals originate from a parallel analysis performed by **Ardian Candra Pratama**, KTH student involved in the same project.

## Technologies

**Python · Pyomo · Gurobi · pandapower · Pandas · NumPy · Matplotlib**

## License

Copyright © 2026 Michelangelo Inzerilli. All rights reserved.

This repository is made publicly available for **portfolio and academic viewing purposes only**. No permission is granted to copy, modify, distribute, or reuse the original code, reports, or other materials developed by the author without prior written permission.

Third-party data and materials, including inputs provided by collaborating companies, external sources, and contributions from other project participants, remain the property of their respective owners and are not covered by this permission.

## Author

**Michelangelo Inzerilli**  
MSc Sustainable Energy Systems  
KTH Royal Institute of Technology