# Numerical Singularity Localization via Adaptive Bisection Method

This repository contains a Python implementation of an adaptive numerical mechanism used to precisely locate an unknown function singularity. The project simulates the classical preprocessing phase required for analyzing the quantum complexity of definite integration for functions with unknown singular points, implementing the mathematical algorithms proposed by Dr. R. Goćwin.

---

## 🔬 Mathematical Background & Problem Statement

The objective is to locate an unknown singularity $\xi_1 = 0.573$ of a function $f(x)$ belonging to the class $F_1^{1,0.5}([a,b])$ over the integration interval $[a,b] = [0.5000, 0.6250]$. The function features a fractional-power cusp (a singularity in its first derivative) and is defined as:

$$f(x) = |x - \xi_1|^{1.5}$$

To find $\xi_1$ without exhaustive grid evaluations, the system implements an **Adaptive Bisection Test ($A_f$)**. The algorithm computes Lagrange polynomial interpolations on adjacent subintervals and utilizes higher-order finite differences to evaluate whether a subinterval contains a derivative disruption. If the difference threshold is breached, a bisection step splits the domain, narrowing down the singularity bounds.

---

## 🚀 Algorithm Workflow

The script operates through the following steps:
1. **Grid Initialization:** Constructing a uniform starting grid across the interval $[a, b]$.
2. **Lagrange Interpolation:** Building localized polynomial approximations to dynamically capture functions variations.
3. **Difference Test ($A_f$) Evaluation:** Calculating the error metric across adjacent nodes to detect structural spikes caused by the cusp.
4. **Adaptive Bisection Loop:** Iteratively halving the suspected interval until the positioning of the singularity $\xi_1$ is locked with high numerical precision.
5. **Visualization:** Plotting the convergent error states, grid intervals, and the target mathematical function.

---

## 📁 Repository Structure

```text
quantum-integration-singularity-finder/
├── O_Kwantowej_Złożoności_Całkowania_Funkcji_z_Nieznaną_Osobliwością.ipynb  # Core Jupyter Notebook project
└── README.md                                                                # Documentation
```
# 🛠️ Requirements & Quick Start

## Prerequisites
To run this notebook, you need a standard Python 3 environment with the following scientific computing libraries installed:

* `numpy`
* `matplotlib`

## How to Run via Google Colab
1. **Upload the notebook:** Upload the `.ipynb` notebook file directly to your Google Drive or open it straight from this GitHub repository.
2. **Configure environment:** Ensure the hardware accelerator runtime is set to **Python 3**.
3. **Execute cells:** Run all cells sequentially (`Ctrl + F9`) to:
   * Execute the grid simulations.
   * Check the convergence data in the terminal output.
   * View the generated visualization charts.

---

# 📚 References & Acknowledgments
This numerical implementation is strictly based on the theoretical frameworks and algorithms detailed in the following academic research regarding the quantum complexity of integration:

* **Goćwin, M.** *ON THE QUANTUM COMPLEXITY OF INTEGRATION
OF A FUNCTION WITH UNKNOWN SINGULARITY*. AGH University of Krakow.
