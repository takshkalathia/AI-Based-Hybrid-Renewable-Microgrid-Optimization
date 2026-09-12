# AI-Based Hybrid Renewable Microgrid Optimization

AI-based optimization and comparative analysis of metaheuristic algorithms for optimal sizing and economic operation of a Solar–Wind–Battery Hybrid Renewable Energy System (HRES).

## Overview

This project investigates the application of metaheuristic optimization techniques to the sizing and economic optimization of a hybrid renewable energy system consisting of photovoltaic (PV), wind turbine (WT), and battery energy storage (BES) components.

The work is organized into two major parts:

1. Comparative evaluation of metaheuristic optimization algorithms using standard benchmark functions and HRES-based performance.
2. PSO-based optimization of the Solar–Wind–Battery HRES to determine an optimal system configuration while minimizing the Net Present Cost (NPC).

The project also analyzes renewable energy generation, load demand, battery dispatch, battery state of charge (SOC), and energy deficit.

---

## Objectives

- Compare the performance of different metaheuristic optimization algorithms.
- Evaluate optimization algorithms using Ackley and Rastrigin benchmark functions.
- Compare algorithm performance for the HRES optimization problem.
- Determine the optimal number of PV panels.
- Determine the optimal number of wind turbines.
- Determine the required battery energy storage capacity.
- Minimize the Net Present Cost (NPC) of the hybrid renewable energy system.
- Analyze renewable generation, load demand, battery operation, and SOC.

---

## System Configuration

The hybrid renewable energy system consists of:

- ☀️ Photovoltaic (PV) generation
- 🌬️ Wind turbine (WT) generation
- 🔋 Battery Energy Storage (BES)
- ⚡ Electrical load demand

The optimization process determines the appropriate sizing of the system components while considering the system's economic performance.

---

## Methodology

### 1. Benchmark Function Comparison

Standard mathematical benchmark functions are used to evaluate the optimization behavior of the implemented algorithms.

The benchmark analysis includes:

- Ackley function
- Rastrigin function

The resulting convergence behavior is analyzed to compare the optimization performance of the algorithms.

### Ackley Function

![Ackley Convergence](results/comparison/ackley_convergence.png)

### Rastrigin Function

![Rastrigin Convergence](results/comparison/rastrigin_convergence.png)

---

## 2. Metaheuristic Algorithm Comparison

Multiple metaheuristic optimization approaches are evaluated for the HRES optimization problem.

The comparison includes algorithms such as:

- Particle Swarm Optimization (PSO)
- Improved Particle Swarm Optimization (IPSO)
- Grey Wolf Optimization (GWO)
- Adaptive/modified optimization approaches used in the study
- Genetic Algorithm (GA)
- BB-BC

The HRES-based comparison focuses on optimization performance and Net Present Cost.

### NPC-Based Algorithm Comparison

![NPC Algorithm Comparison](results/comparison/npc_algorithm_comparison.png)

### Detailed PSO, ABSO and GWO Comparison

The comparison study produced the following HRES sizing and economic results:

| Parameter | PSO | ABSO | GWO |
|---|---:|---:|---:|
| PV Panels | 303 | 320 | 311 |
| PV Cost ($) | 94,630 | 99,940 | 97,129 |
| Wind Turbines | 257 | 264 | 267 |
| Wind Cost ($) | 705,778 | 725,002 | 733,241 |
| Battery Capacity (kWh) | 2,870 | 2,808 | 2,795 |
| Battery Cost ($) | 1,148,000 | 1,123,200 | 1,118,000 |
| Penalty Cost ($) | 73 | 9,132 | 6,460 |
| **Total NPC ($)** | **1,948,481** | **1,957,265** | **1,954,830** |

Among the three compared approaches, PSO obtained the lowest Total NPC of **$1,948,481**.

---

## 3. PSO-Based HRES Optimization

PSO is applied to optimize the sizing of the Solar–Wind–Battery hybrid renewable energy system.

The optimization determines:

- Number of PV panels
- Number of wind turbines
- Battery capacity
- Net Present Cost (NPC)

### Optimal Configuration Obtained Using PSO

| Component | Optimal Value |
|---|---:|
| PV Panels | 303 |
| Wind Turbines | 257 |
| Battery Capacity | 2,870 kWh |
| Total NPC | $1,948,481 |

The optimized system is further evaluated through renewable generation, load demand, battery dispatch, SOC, and energy deficit analysis.

---

## Results

### PSO Convergence

![PSO Convergence](results/optimization/pso_convergence.png)

### Renewable Generation and Load

![Generation vs Load](results/optimization/generation_vs_load.png)

### Solar Generation

![Solar Generation](results/optimization/solar_generation.png)

### Wind Generation

![Wind Generation](results/optimization/wind_generation.png)

### Load Profile

![Load Profile](results/optimization/load_profile.png)

### Battery Dispatch

![Battery Dispatch Profile](results/optimization/battery_dispatch_profile.png)

### Battery State of Charge

![Battery SOC](results/optimization/battery_soc.png)

### Energy Deficit

![Energy Deficit](results/optimization/energy_deficit.png)

### Optimization Results

![Optimization Results Table](results/optimization/optimization_results_table.png)

---

## Dataset

The project uses a renewable energy and load dataset containing time-series information for the hybrid renewable energy system.

The dataset contains the following variables:

| Variable | Description |
|---|---|
| `timestamp` | Date and time of the observation |
| `solar_irradiance` | Solar irradiance |
| `wind_speed` | Wind speed |
| `temperature` | Temperature |
| `humidity` | Relative humidity |
| `atmospheric_pressure` | Atmospheric pressure |
| `grid_load_demand` | Electrical load demand |

The dataset is available in:

```text
data/renewable_microgrid_dataset.csv
