# Extended Halfway Escape Optimization (HEO)

This repository provides a reproducible implementation and experimental study of **extended variants of the Halfway Escape Optimization (HEO) algorithm**, including stabilization, evolutionary strategies, immune-inspired mutation, and directional mutation mechanisms.

The work is based on the original HEO paper and extends it through systematic algorithmic modifications and benchmarking.

---

## 📌 Project Overview

Halfway Escape Optimization (HEO) is a population-based metaheuristic designed to avoid premature convergence by enforcing exploration through escape mechanisms.

While effective in maintaining diversity, the original HEO algorithm exhibits weak convergence behavior near optimal regions. This project investigates and improves these limitations through several extensions:

- Removal of unstable stochastic amplification terms
- Introduction of convergent vibration mechanisms
- Integration of Evolution Strategies (1/5 success rule)
- Immune-inspired adaptive mutation (CIBA)
- Directional affinity-based mutation (DirCIBA)
- Evaluation on both zero-minimum and non-zero benchmark functions

---

## 🔬 Implemented Variants

The following HEO variants are implemented and evaluated:

| Variant | Description |
|---------|-------------|
| Original HEO | Baseline algorithm as proposed in the original paper |
| v2 (HEO + ES) | Stabilized HEO with convergent vibration and ES (1/5 rule) |
| HEO + CIBA | Immune-inspired affinity-controlled mutation |
| HEO + DirCIBA | Directional affinity-controlled mutation |
| HEO + ES + CIBA | Hybrid exploitation–exploration variants |

---

## 📊 Benchmarks

The algorithms are evaluated on standard 30-dimensional benchmark functions:

### Zero-Minimum Functions
- Sphere
- Rosenbrock
- Rastrigin
- Griewank
- Levy
- Ackley
- Schwefel
- Bent Cigar
- Alpine
- Salomon

### Non-Zero (Shifted + Offset) Functions
- Shifted Sphere
- Shifted Rastrigin
- Shifted Rosenbrock
- Shifted Griewank
- Shifted Levy

Non-zero benchmarks are constructed as:
f_shift(x) = f(x - s) + c

where `s` is a random shift vector and `c` is a positive offset.

---

## ⚙️ Experimental Setup

All experiments were conducted using the following configuration:

- Dimension: 30
- Population size: 100
- Iterations: 1000
- Independent runs: 30
- Boundary: [-100, 100]
- Evaluation metric: Mean and standard deviation of best fitness

All experiments are reproducible using fixed random seeds.

📚 References
---
Original HEO:

Halfway Escape Optimization: A Novel Metaheuristic Algorithm for Global Optimization, arXiv:2405.02850

Rechenberg, I. (1973). Evolutionsstrategie.

de Castro, L. N., & Von Zuben, F. J. (2002). Artificial Immune Systems.

📝 Citation
---
If you use this code in your research, please cite:

```
@article{yourname2025heo,
  title   = {Extended Halfway Escape Optimization with Adaptive Mutation},
  author  = {Ali Soltani},
  journal = {Preprint},
  year    = {2025}
}
```

📄 License
---
This project is released under the MIT License. See LICENSE for details.

👤 Author
---
Ali Soltani

Department of CE

Amirkabir University (Tehran polytechnic)

Email: ali.soltani@aut.ac.ir

⚠️ Disclaimer
---
This repository is intended for research and educational purposes. The implementations are experimental and may require further tuning for specific applications.
