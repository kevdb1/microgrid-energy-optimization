# Microgrid Energy Optimization

An independent summer learning project completed after my first year at the University of Illinois Urbana-Champaign.

[Open the notebook in Google Colab](https://colab.research.google.com/github/kevdb1/microgrid-energy-optimization/blob/main/Microgrid_Project_26Summer.ipynb)

## Overview

In this project, I used Python, PyPSA, and the HiGHS solver to explore how renewable generation, battery storage, transmission limits, and carbon prices affect a simplified power system.

I started with a basic 24-hour dispatch model and gradually added four extensions:

1. Hefei solar and wind generation data
2. Generation and battery capacity expansion
3. A two-bus transmission-congestion model
4. Carbon-tax sensitivity analysis

The main goal was to learn how power-system optimization models are built, solved, visualized, and interpreted.

## Tools

- Python
- PyPSA
- HiGHS
- pandas
- NumPy
- matplotlib
- Google Colab

## Data

The solar and wind profiles were obtained from Renewables.ninja for Hefei, China.

The original timestamps are in UTC and are converted to China Standard Time (UTC+8) in the notebook.

- [`hf_solar.csv`](hf_solar.csv)
- [`hf_wind.csv`](hf_wind.csv)

## Results

### 1. Hefei Energy Dispatch and Electricity Price

This scenario shows hourly demand, renewable generation, thermal generation or grid imports, battery operation, and marginal electricity prices.

![Hefei energy dispatch and LMP](01_hefei_dispatch_lmp.png)

### 2. Capacity Expansion

This model allows the optimizer to select the capacities of thermal generation, solar, wind, and battery storage under simplified cost and capacity assumptions.

![Capacity expansion optimization](02_capacity_expansion_lmp.png)

### 3. Transmission Congestion

This two-bus example shows how a limited transmission line can create different electricity prices at different locations.

![Transmission congestion and LMP](03_transmission_congestion_lmp.png)

### 4. Carbon-Tax Sensitivity

This scenario compares how different carbon prices affect thermal generation, renewable capacity, battery deployment, and emissions.

![Carbon-tax sensitivity](04_carbon_tax_sensitivity.png)

## What I Learned

- How to build basic power-system models with PyPSA
- How to formulate hourly supply-and-demand constraints
- How battery storage shifts energy between time periods
- How transmission congestion affects nodal electricity prices
- How to compare capacity and carbon-policy scenarios
- How to visualize and explain optimization results

## Project Files

- [`Microgrid_Project_26Summer.ipynb`](Microgrid_Project_26Summer.ipynb) — complete Colab notebook
- [`Microgrid_Optimization_Report.pdf`](Microgrid_Optimization_Report.pdf) — English project report
- [`hf_solar.csv`](hf_solar.csv) — solar-generation data
- [`hf_wind.csv`](hf_wind.csv) — wind-generation data

## How to Run

1. Open the notebook using the Google Colab link above.
2. Run the package-installation cell.
3. Upload `hf_solar.csv` and `hf_wind.csv` when prompted.
4. Run the remaining cells in order.

## Note

This is a learning project based on simplified demand, cost, and technology assumptions. It is intended to demonstrate the modeling process rather than provide a real-world power-system forecast.

## Author

Yuming (William) Bian  
University of Illinois Urbana-Champaign
