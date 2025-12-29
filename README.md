# SVD-Based Characterization of Metaheuristic Algorithms

This repository contains a practical implementation and analysis of an **SVD-based pipeline for characterizing metaheuristic optimization algorithms**, inspired directly by the methodology described in the referenced research paper included in this repository.

The goal of this project is **not** to identify a single best optimization algorithm, but to **analyze, compare, and cluster algorithms based on their observed performance behavior** across standard benchmark functions.

---

## Project Overview

**Title:** A Practical Analysis of Metaheuristic Algorithm Behavior using SVD  
**Authors:**  
- K. Anshul Reddy (U23AI107)  
- Mihir Hajare (U23AI092)  

This project is a mini, hands-on reproduction of the analysis pipeline proposed in the research paper:

> *Characterization of CEC Single-Objective Optimization Competition Benchmarks and Algorithms* (2023)

The original paper itself is provided in this repository and serves as the **primary reference** for both methodology and interpretation.

---

## What This Project Does

The project evaluates and compares four popular metaheuristic algorithms by running them on multiple benchmark optimization functions and then applying linear algebra and clustering techniques to uncover latent behavioral patterns.

### Algorithms Implemented
- Particle Swarm Optimization (PSO)
- Differential Evolution (DE)
- Genetic Algorithm (GA)
- Simulated Annealing (SA)

### Benchmark Functions
- Sphere Function
- Ackley Function
- Rastrigin Function

All benchmarks are evaluated in **5 dimensions**.

---

## Analysis Pipeline

The implementation follows the same logical stages as described in the reference paper:

1. **Performance Matrix (P)**
   - Raw best fitness values obtained by each algorithm on each benchmark.

2. **Rank Matrix (R)**
   - Performance normalized by converting raw scores into ranks (row-wise).

3. **Singular Value Decomposition (SVD)**
   - SVD applied to the Rank Matrix to extract latent behavioral features.

4. **Hierarchical Clustering**
   - Algorithms and benchmarks are clustered based on their SVD feature vectors.
   - Results visualized using dendrograms.

This pipeline enables **data-driven algorithm comparison** beyond design-level descriptions.

---

## Repository Contents

- `802d46ce-8aec-4046-b143-c8e6ea68b8a8.pdf`  
  → Reference research paper describing the original methodology.

- `Project.ipynb`  
  → Jupyter Notebook containing:
  - Benchmark function implementations  
  - Metaheuristic algorithm implementations  
  - Performance and rank matrix construction  
  - SVD computation  
  - Hierarchical clustering and analysis  

- `README.md`  
  → Project overview and documentation.

Readers are encouraged to go through the **notebook alongside the paper** for a clearer understanding of how theory translates into practice.

---

## Key Findings

- **SVD is effective** at extracting meaningful behavioral features from performance data.
- Results support the **No Free Lunch Theorem** — no algorithm dominates across all benchmarks.
- **Convergence behavior matters**, not just final fitness values.
- Algorithms with different designs may still show similar performance patterns when analyzed empirically.

---

## Limitations

- Only a **single run per algorithm-function pair** was performed (due to scope constraints).
- Metaheuristic performance is **highly stochastic**.
- Hyperparameter tuning was limited to standard textbook values.

The reference paper discusses these issues in depth and recommends multi-run statistical analysis for rigorous studies.

---

## Intended Audience

- AI and Machine Learning students
- Optimization and Metaheuristics researchers
- Readers interested in algorithm behavior analysis
- Anyone studying performance-based algorithm characterization

---

## Reference

The complete methodology and theoretical motivation for this project are documented in the research paper included in this repository. This implementation closely follows that work and is intended as a **learning-oriented, reproducible demonstration** rather than a full-scale experimental study.
