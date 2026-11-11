# ATMIQ HACKATHON
# Hybrid Intelligence: Classical Machine Learning and Quantum Optimization

### A Comparative Study of Classical Optimization and the Quantum Approximate Optimization Algorithm (QAOA)

## 1. Project Overview 

This project explores the application of classical optimization and quantum computing to a constrained customer-selection problem.

It compares a classically optimized solution against the Quantum Approximate Optimization Algorithm (QAOA) using quantum circuit simulation and statevector probability analysis.

The primary objective is to investigate how quantum optimization performs against a rigorously verified classical benchmark while evaluating solution quality, feasibility, and sensitivity to changing resource constraints.

The project was developed as part of the **ATMIQ Hackathon 2026**.

## 2. Problem Statement

The optimization problem involves selecting a fixed number of customers from a given customer pool while satisfying budget and capacity constraints.

The objective is to maximize the overall selection objective without violating the specified constraints.

### Problem Configuration

| Parameter | Value |
|---|---:|
| Total customers | 10 |
| Required selections | 6 |
| Baseline budget | 25 |
| Baseline capacity | 22 |
| Total combinations evaluated | 210 |

Two optimization approaches are investigated:

- **Classical Optimization:** Exhaustive evaluation of all possible customer combinations to identify the global optimum.
- **Quantum Optimization:** QAOA-based optimization formulation evaluated through quantum statevector simulation.

## 3. Classical Optimization Results

The classical optimizer evaluated all 210 possible customer combinations and identified the best verified solution.

| Metric | Result |
|---|---:|
| Optimal customer selection | [1, 2, 3, 4, 5, 6] |
| Optimal objective value | 25.3068911090 |
| Combinations evaluated | 210 |
| Exhaustive verification | Passed |

The classical solution serves as the benchmark for evaluating the performance of the QAOA implementation.

## 4. Quantum Optimization Using QAOA

The Quantum Approximate Optimization Algorithm was implemented to investigate the customer-selection problem using a quantum circuit representation.

The quantum simulation was evaluated through statevector probabilities, objective calculations, and feasibility analysis.

### Quantum Configuration and Results

| Metric | Result |
|---|---:|
| Total qubits | 20 |
| Statevector dimension | 1,048,576 |
| Conditional expected objective | 11.4063238956 |
| Objective quality | 45.0720% |
| Relative objective gap | 54.9280% |
| Feasible probability | 24.9352% |

### Classical vs Quantum Comparison

| Metric | Classical Optimization | QAOA |
|---|---:|---:|
| Objective value | 25.306891 | 11.406324 |
| Relative objective quality | 100% | 45.0720% |

The results indicate that the current classical optimizer outperforms the QAOA implementation for the tested configuration.

## 5. Sensitivity Analysis

A sensitivity analysis was performed to evaluate the stability of the optimization model under different budget and capacity constraints.

| Metric | Result |
|---|---:|
| Budget-capacity scenarios evaluated | 121 |
| Scenarios with feasible solutions | 121 |
| Baseline optimal selection stability | 90.9091% |

This analysis provides insight into the robustness of the optimization solution and its response to changing resource constraints.

## 6. Prerequisites

Before running the project, ensure that the following software and libraries are available.

### Software Requirements

- Python 3.10 or compatible version
- Google Colab or Jupyter Notebook
- Internet connection for installing dependencies
- Sufficient RAM for quantum statevector simulation

### Required Python Libraries

- NumPy
- Pandas
- SciPy
- Matplotlib
- Seaborn
- Qiskit
- Qiskit Aer

### Hardware Recommendations

- Minimum 8 GB RAM recommended
- 16 GB RAM or higher recommended for more comfortable statevector simulation
- Multi-core processor recommended

**Note:** The 20-qubit statevector contains 1,048,576 complex amplitudes. Memory requirements depend on data types, simulator implementation, and additional intermediate arrays.

## 7. Installation and Setup

### Option 1: Google Colab (Recommended)

1. Open Google Colab.
2. Upload `Classical_ML.ipynb` or open it from Google Drive.
3. Select a Python runtime.
4. Install the required dependencies in a notebook cell.

Example installation command:

```python
!pip install numpy pandas scipy matplotlib seaborn qiskit qiskit-aer
```

5. Run the notebook cells sequentially.
6. Verify the classical optimization results.
7. Execute the QAOA simulation and validation cells.
8. Review the generated reports and visualizations.

### Option 2: Local Jupyter Notebook

Clone the project repository or download the notebook.

Install the dependencies:

```bash
pip install numpy pandas scipy matplotlib seaborn qiskit qiskit-aer
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `Classical_ML.ipynb` and execute the cells sequentially.

**Note:** Exact dependency versions may vary. For reproducibility, use compatible versions of the libraries and the same configuration used during the original experiment.

## 8. Project Structure

```text
ATMIQ_HACKATHON/
│
├── Classical_ML.ipynb
│
├── results/
│   ├── JSON reports
│   ├── CSV result tables
│   └── Optimization visualizations
│
└── README.md
```

The results directory represents the exported experiment outputs. Actual filenames may differ depending on the notebook execution and export configuration.

## 9. Validation and Verification

The final validation process covered the following components:

- Classical optimization benchmark verification.
- Exhaustive combination evaluation.
- QAOA statevector dimension verification.
- Quantum probability normalization.
- Feasibility probability analysis.
- Budget-capacity sensitivity analysis.
- Final benchmark verification.
- Results and visualization exports.

The validation process helps ensure that the reported experimental results are consistent with the implemented optimization model.

## 10. Key Findings

The experiment demonstrates several important observations:

1. Classical exhaustive optimization successfully identified the best solution for the tested problem.
2. QAOA provided an alternative quantum optimization framework for the same problem.
3. The current QAOA implementation achieved 45.0720% of the classical benchmark objective.
4. The measured feasible probability was 24.9352%.
5. Sensitivity analysis showed 90.9091% baseline optimal selection stability.

**Research limitation:** These experimental results do not demonstrate quantum advantage or quantum speedup. The classical approach remains superior for the tested problem configuration.

## 11. Future Improvements

Potential directions for further development include:

- Improving QAOA parameter optimization.
- Experimenting with different circuit depths and QAOA layers.
- Refining penalty coefficients and constraint encoding.
- Exploring alternative quantum optimization algorithms.
- Investigating hardware-based quantum execution.
- Evaluating larger customer-selection problems.
- Comparing quantum and classical performance across multiple problem sizes.

## 12. Technologies Used

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Quantum Framework | Qiskit |
| Quantum Simulation | Qiskit Aer |
| Numerical Computing | NumPy, SciPy |
| Data Processing | Pandas |
| Data Visualization | Matplotlib, Seaborn |
| Development Environment | Google Colab, Jupyter Notebook |
| Optimization Approach | Classical Exhaustive Search, QAOA |

## 13. Conclusion

This project presents an experimental comparison between classical optimization and quantum optimization using QAOA for a constrained customer-selection problem.

The classical optimizer established a verified benchmark, while the QAOA implementation provided an opportunity to investigate quantum state probabilities, feasibility, and optimization performance.

Although the current QAOA results do not outperform the classical benchmark, the experiment provides a foundation for further research into hybrid classical-quantum optimization approaches.

The broader objective is to understand where quantum algorithms may complement classical computational techniques and how hybrid optimization strategies can contribute to solving increasingly complex decision-making problems.

---

**Project:** ATMIQ HACKATHON 2026

**Focus Areas:** Classical Optimization, Quantum Computing, QAOA, Hybrid Intelligence, Combinatorial Optimization

**Core Objective:** Evaluating quantum optimization against a verified classical benchmark.
