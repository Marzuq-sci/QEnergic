# Q-Energic: Quantum-Inspired Microgrid Optimization

**Q-Energic** is an end-to-end optimization pipeline designed to solve complex rural electrification site-selection problems. This repository specifically focuses on a **50-site case study in Ethiopia**, leveraging Quantum-Inspired Simulated Annealing to balance capital expenditure, population coverage, and energy generation potential.

## 🚀 Framework Architecture

The framework is structured into a 4-Layer pipeline to ensure reproducibility and mathematical rigor:

* **Layer 1: Data Acquisition** - Ingests verified Ethiopian geospatial metadata.
* **Layer 2: QUBO Construction** - Maps multi-objective constraints to a Quadratic Unconstrained Binary Optimization (QUBO) form.
* **Layer 3: Solver Execution** - Utilizes the `dwave-neal` simulated annealer to navigate a search space of $2^{50}$ configurations.
* **Layer 4: Evaluation** - Performs symbolic verification (SymPy) and generates high-fidelity vector visualizations (Matplotlib).

## 📊 Key Results (Ethiopia Dataset)

Based on the current verified dataset, the Q-Energic framework achieved:

* **Population Covered:** 5,380 (Exceeding the 5,000 target).
* **Budget Spent:** $725,000 (19.4% budget surplus).
* **Efficiency Metric:** ~$134.76 per person served.
* **Verification:** 100% uniqueness audit pass (No duplicate site selection).

## 🛠️ Installation & Usage

### Prerequisites

```bash
pip install dwave-ocean-sdk sympy matplotlib pandas

```

### Running the Optimizer

You can run the full pipeline in Google Colab or locally:

1. Clone the repository: `git clone https://github.com/Marzuq-sci/QEnergic.git`
2. Run the notebook/script: `python q_energic_main.py`

## 📈 Convergence Profile

The framework generates a **Relative Hamiltonian Energy** distribution. The convergence to the ground state ($E - E_{min} = 0$) demonstrates the robustness of the penalty weights used in the multi-objective formulation.
