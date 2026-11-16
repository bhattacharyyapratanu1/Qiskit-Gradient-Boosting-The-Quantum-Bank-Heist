<!-- ======================================================= -->
<!--                  ATMIQ HACKATHON 2026                 -->
<!-- ======================================================= -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:080B1A,45:302B75,100:00C9D8&height=230&section=header&text=HYBRID%20INTELLIGENCE&fontSize=43&fontColor=FFFFFF&fontAlignY=40&animation=fadeIn&desc=CLASSICAL%20OPTIMIZATION%20%7C%20QUANTUM%20COMPUTING&descSize=15&descAlignY=59&descColor=C8D7FF" width="100%" alt="Hybrid Intelligence animated banner"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=18&duration=3000&pause=1000&color=00D9FF&center=true&vCenter=true&width=750&lines=Exploring+the+Future+of+Hybrid+Optimization;Classical+Intelligence+meets+Quantum+Computing;Benchmarking+QAOA+Against+Classical+Optimization;An+Experimental+Study+in+Quantum+Algorithms" alt="Animated project introduction"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/EVENT-ATMIQ%20HACKATHON%202026-635BFF?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/DOMAIN-QUANTUM%20COMPUTING-00B8D9?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/ALGORITHM-QAOA-8957E5?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/LANGUAGE-PYTHON-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
</p>

<p align="center">
  <b>A Comparative Study of Classical Optimization and the Quantum Approximate Optimization Algorithm</b>
</p>

---

## 01. Research Overview

What happens when classical optimization meets quantum computing?

**HYBRID INTELLIGENCE** investigates this question through a constrained customer-selection problem, comparing an exhaustive classical optimization strategy against the Quantum Approximate Optimization Algorithm (QAOA).

The research establishes a verified classical benchmark and evaluates the quantum implementation through circuit simulation, statevector probability analysis, objective evaluation and constraint feasibility.

The experiment focuses on three fundamental questions:

- How effectively can QAOA approximate a constrained optimization solution?
- How does its solution quality compare with an exhaustive classical benchmark?
- How stable is the optimization model when resource constraints change?

Rather than presuming quantum superiority, the project evaluates both approaches using measurable experimental results.

<p align="center">
  <img src="assets/quantum-computing.gif" width="85%" alt="Quantum computing research animation"/>
</p>

<p align="center">
  <sub>Conceptual visualization of quantum computation and hybrid optimization.</sub>
</p>

---

## 02. The Optimization Challenge

The experiment considers a customer-selection problem in which exactly six customers must be selected from a pool of ten.

The selected combination must satisfy two resource constraints:

- Budget limitation.
- Capacity limitation.

The objective is to maximize the overall selection value while maintaining feasibility.

### Experimental Parameters

| Parameter | Value |
|:---|---:|
| Customer pool | 10 |
| Required selections | 6 |
| Baseline budget | 25 |
| Baseline capacity | 22 |
| Search space | 210 combinations |

The total classical search space is:

\[
\binom{10}{6}=210
\]

Every possible six-customer combination is evaluated by the classical benchmark.

---

## 03. Two Optimization Paradigms

<p align="center">
  <img src="assets/hybrid-architecture.gif" width="95%" alt="Hybrid classical quantum optimization architecture"/>
</p>

### Classical Optimization

The classical approach uses exhaustive combinatorial search to evaluate all 210 possible selections.

It identifies the best feasible combination and establishes the reference objective for the quantum experiment.

| Evaluation | Result |
|:---|---:|
| Optimal selection | `[1, 2, 3, 4, 5, 6]` |
| Optimal objective | **25.3068911090** |
| Combinations evaluated | 210 |
| Exhaustive verification | Passed |

### Quantum Optimization

The quantum approach uses the Quantum Approximate Optimization Algorithm (QAOA).

The implementation evaluates a quantum statevector and analyzes the resulting probability distribution, objective quality and feasibility.

| Configuration | Result |
|:---|---:|
| Qubits | 20 |
| Statevector dimension | 1,048,576 |
| Conditional expected objective | 11.4063238956 |
| Objective quality | 45.0720% |
| Relative objective gap | 54.9280% |
| Feasible probability | 24.9352% |

The simulated state space contains:

\[
2^{20}=1,048,576
\]

complex probability amplitudes.

---

## 04. Experimental Performance

### Classical vs Quantum

<p align="center">
  <img src="assets/classical-vs-quantum.gif" width="95%" alt="Animated classical versus quantum performance comparison"/>
</p>

| Performance Metric | Classical | QAOA |
|:---|---:|---:|
| Objective value | 25.306891 | 11.406324 |
| Relative objective quality | 100% | 45.0720% |
| Optimization method | Exhaustive Search | QAOA |
| Global optimum verified | Yes | Not established |

### Objective Quality

\[
\text{Objective Quality}=
\frac{11.4063238956}{25.3068911090}\times100
\]

<p align="center">
  <img src="https://img.shields.io/badge/CLASSICAL%20BENCHMARK-100%25-168B72?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/QAOA%20QUALITY-45.0720%25-7657D5?style=for-the-badge"/>
</p>

The current QAOA implementation achieved 45.0720% of the classical benchmark objective.

The results indicate that classical exhaustive optimization outperformed the current quantum implementation under the tested configuration.

---

## 05. Quantum Statevector Analysis

<p align="center">
  <img src="assets/quantum-statevector.gif" width="95%" alt="Quantum statevector probability distribution animation"/>
</p>

The quantum simulation evaluates the probability amplitudes associated with the computational basis states.

The statevector is used to investigate:

- Quantum state probabilities.
- Distribution of candidate solutions.
- Objective values associated with candidate states.
- Constraint feasibility.
- Probability normalization.

This analysis provides insight into how the quantum optimization formulation distributes probability across possible computational states.

---

## 06. Constraint Feasibility

<p align="center">
  <img src="assets/feasibility-analysis.gif" width="90%" alt="Animated feasibility analysis"/>
</p>

A feasible solution must satisfy the selection, budget and capacity constraints.

The reported feasible probability is:

<p align="center">
  <img src="https://img.shields.io/badge/FEASIBLE%20PROBABILITY-24.9352%25-00A6C8?style=for-the-badge"/>
</p>

This result highlights the importance of constraint encoding and penalty optimization when implementing QAOA for constrained combinatorial problems.

---

## 07. Sensitivity Analysis

<p align="center">
  <img src="assets/sensitivity-analysis.gif" width="95%" alt="Animated budget capacity sensitivity analysis"/>
</p>

The optimization model was evaluated under different budget and capacity configurations to investigate the stability of the optimal selection.

| Metric | Result |
|:---|---:|
| Scenarios evaluated | 121 |
| Scenarios with feasible solutions | 121 |
| Baseline optimal selection stability | 90.9091% |

The results demonstrate how the optimal selection responds to variations in available resources.

---

## 08. Mathematical Formulation

Let each customer be represented by a binary decision variable:

\[
x_i\in\{0,1\}
\]

Where:

- \(x_i=1\): Customer selected.
- \(x_i=0\): Customer not selected.

The selection constraint is:

\[
\sum_{i=1}^{10}x_i=6
\]

The general optimization objective is:

\[
\max \sum_{i=1}^{10}v_i x_i
\]

Subject to:

**Budget constraint**

\[
\sum_{i=1}^{10}b_i x_i\leq25
\]

**Capacity constraint**

\[
\sum_{i=1}^{10}c_i x_i\leq22
\]

Where:

- \(v_i\) represents the objective contribution.
- \(b_i\) represents budget consumption.
- \(c_i\) represents capacity consumption.

This is the general mathematical representation; the exact coefficients and QAOA constraint encoding are determined by the notebook implementation.

---

## 09. Technology Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,numpy,scipy,git,github" alt="Technology stack"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/QISKIT-6929C4?style=flat-square"/>
  <img src="https://img.shields.io/badge/QISKIT%20AER-6929C4?style=flat-square"/>
  <img src="https://img.shields.io/badge/PANDAS-150458?style=flat-square"/>
  <img src="https://img.shields.io/badge/MATPLOTLIB-11557C?style=flat-square"/>
  <img src="https://img.shields.io/badge/SEABORN-4385B5?style=flat-square"/>
  <img src="https://img.shields.io/badge/JUPYTER-F37626?style=flat-square"/>
</p>

| Layer | Technology |
|:---|:---|
| Programming | Python |
| Quantum Framework | Qiskit |
| Quantum Simulator | Qiskit Aer |
| Numerical Computing | NumPy, SciPy |
| Data Processing | Pandas |
| Visualization | Matplotlib, Seaborn |
| Development | Google Colab, Jupyter Notebook |
| Classical Method | Exhaustive Search |
| Quantum Method | QAOA |

---

## 10. Installation and Execution

### Requirements

- Python 3.10 or compatible version.
- Google Colab or Jupyter Notebook.
- Minimum 8 GB RAM recommended.
- 16 GB RAM or higher recommended for more comfortable simulation.

### Google Colab

1. Open Google Colab.
2. Upload `Classical_ML.ipynb`.
3. Install the required dependencies.

```python
!pip install numpy pandas scipy matplotlib seaborn qiskit qiskit-aer
```

4. Execute the notebook cells sequentially.
5. Run the classical optimization benchmark.
6. Execute the QAOA simulation.
7. Review the generated results and visualizations.

### Local Installation

Clone the repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Navigate to the project:

```bash
cd ATMIQ_HACKATHON
```

Install dependencies:

```bash
pip install numpy pandas scipy matplotlib seaborn qiskit qiskit-aer
```

Launch Jupyter:

```bash
jupyter notebook
```

Open `Classical_ML.ipynb` and execute the notebook.

---

## 11. Repository Architecture

```text
ATMIQ_HACKATHON/
│
├── Classical_ML.ipynb
│
├── assets/
│   ├── quantum-computing.gif
│   ├── hybrid-architecture.gif
│   ├── classical-vs-quantum.gif
│   ├── quantum-statevector.gif
│   ├── feasibility-analysis.gif
│   └── sensitivity-analysis.gif
│
├── results/
│   ├── reports/
│   ├── tables/
│   └── visualizations/
│
├── requirements.txt
│
└── README.md
```

The structure represents the recommended organization. Include only files that actually exist in the repository.

---

## 12. Validation and Verification

The experimental validation covers:

| Validation | Purpose |
|:---|:---|
| Exhaustive search | Evaluate all 210 combinations |
| Classical benchmark | Verify the best solution |
| Statevector dimension | Check the 20-qubit simulation |
| Probability normalization | Validate the probability distribution |
| Feasibility analysis | Evaluate constraint satisfaction |
| Sensitivity analysis | Examine resource stability |
| Result exports | Preserve experiment outputs |

---

## 13. Research Findings

The experiment produces several important observations.

**Classical optimization establishes a verified benchmark.**

Exhaustive search identifies the best feasible solution for the tested problem.

**QAOA provides an alternative optimization framework.**

Quantum statevector simulation allows the investigation of probability distributions and feasibility.

**The current classical approach performs better.**

The QAOA implementation achieved 45.0720% of the classical benchmark objective.

**Constraint satisfaction remains challenging.**

The reported feasible probability is 24.9352%.

**The model demonstrates sensitivity stability.**

The baseline optimal selection stability is 90.9091% across the evaluated scenarios.

### Research Limitation

The results do not establish quantum advantage or quantum speedup.

For the tested configuration, classical exhaustive optimization remains superior.

---

## 14. Future Research

Potential research directions include:

- Increasing QAOA circuit depth.
- Improving variational parameter optimization.
- Refining penalty coefficients and constraint encoding.
- Exploring alternative quantum optimization algorithms.
- Evaluating quantum hardware execution.
- Scaling the customer-selection problem.
- Comparing against additional classical optimization techniques.
- Studying convergence, computational cost and solution quality.

---

## 15. Project Information

| Attribute | Details |
|:---|:---|
| Project Title | HYBRID INTELLIGENCE |
| Event | ATMIQ HACKATHON 2026 |
| Research Area | Hybrid Intelligence |
| Primary Algorithm | QAOA |
| Classical Benchmark | Exhaustive Search |
| Quantum Simulation | Statevector |
| Programming Language | Python |

---

## Conclusion

**HYBRID INTELLIGENCE** investigates the intersection of classical optimization and quantum computing through a measurable experimental comparison.

The classical optimizer establishes a verified benchmark, while QAOA provides an alternative quantum framework for investigating constrained combinatorial optimization.

Although the current quantum implementation does not outperform the classical approach, the experiment provides valuable insight into quantum probability distributions, feasibility, optimization quality and resource sensitivity.

The research emphasizes a fundamental principle:

> The future of optimization should be driven by measurable computational performance, rigorous benchmarking and intelligent integration of classical and quantum techniques.

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00C9D8,50:302B75,100:080B1A&height=130&section=footer&animation=fadeIn" width="100%" alt="Animated footer"/>
</p>

<p align="center">
  <b>ATMIQ HACKATHON 2026</b>
  <br/>
  <sub>CLASSICAL INTELLIGENCE. QUANTUM POSSIBILITIES. HYBRID FUTURE.</sub>
</p>
