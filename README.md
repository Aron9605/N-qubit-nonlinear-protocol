# N-Qubit Nonlinear Protocol for GHZ-State Distillation

Numerical and symbolic implementations of nonlinear protocols for distilling
Greenberger–Horne–Zeilinger (GHZ) states.

This repository accompanies:

> Áron Rozgonyi, Gábor Széchenyi, Orsolya Kálmán, and Tamás Kiss,  
> **“Practical scheme for efficient distillation of GHZ states.”**  
> arXiv:2501.12268  
> https://doi.org/10.48550/arXiv.2501.12268

## Overview

<p align="justify">
Generating high-fidelity multipartite entangled states is challenging because
state preparation, quantum gates, and measurements are affected by coherent and
incoherent noise. Entanglement distillation addresses this problem by
probabilistically transforming multiple imperfect states into fewer states with
higher fidelity.

This repository investigates iterative, postselection-based distillation
protocols for N-qubit GHZ states. The protocols use local unitary operations,
computational-basis measurements, and classical communication to suppress
errors and increase fidelity with the target state
</p>

$$
\lvert \mathrm{GHZ} \rangle_N =
\frac{\lvert 0 \rangle^{\otimes N} +
      \lvert 1 \rangle^{\otimes N}}{\sqrt{2}}.
$$


<p align="justify">
Our scheme remains practical by employing a limited set of straightforward unitary operations and projective measurements in the computational basis, resulting in subexponential convergence to a pure GHZ state, similarly to the recent scheme for two-qubit Bell states[2].
We systematically develop a double-iteration protocol by establishing a mathematical framework for the transformation processes, with particular emphasis on the role of unitary operations in correcting small arbitrary errors in the initial states. Most importantly, our scheme can probabilistically transform 4 input copies of noisy GHZ states into a single, almost-perfect GHZ state, eliminating noise to first order. We also analytically derive a corresponding no-go theorem by demonstrating that such a scheme is impossible if only 2 inputs are provided. 
Notably, our protocol corrects small arbitrary distortions in GHZ states, converging subexponentially to a pure GHZ state while maintaining operational simplicity, thereby supporting its feasibility for practical quantum computing applications.
</p>

The included notebooks cover:

- numerical simulation of alternating CXX and CXH distillation rounds;
- memory-efficient evaluation without constructing a dense joint
  \(2N\)-qubit density matrix;
- comparison of fidelity and postselection probability across system sizes;
- investigation of depolarizing and other noise models;
- symbolic analysis of the three-qubit protocol;
- unitary construction, noise analysis, and the two-copy no-go result.

*References*:

> [1] Áron Rozgonyi, Gábor Széchenyi, Orsolya Kálmán, Tamás Kiss.  
> **Training iterated protocols for distillation of GHZ states with variational quantum algorithms.** Physics Letters A, Volume 499, 5 March 2024, 129349. 
> https://doi.org/10.1016/j.physleta.2024.129349

> [2] Kálmán, O., Gábris, A., Jex, I., & Kiss, T. (2025, December).  
> **Universal, unambiguous concentration and distillation of Bell pairs.** Physical Review Letters, 135(26), 260202.  
> https://doi.org/10.1103/rcx1-w6j7 

## Repository Contents

```t
.
├── AUTHORS.md
├── CITATION.cff
├── README.md
└── notebooks                           # Source code for implementing the quantum protocols.
    ├── 3qubit_symbolic.nb              # Symbolic analysis of the 3-qubit protocol, unitary construction, no-go theorem
    ├── NGHZ_distill.ipynb              # Memory-efficient simulation of the alternating N-qubit protocol
    └── n_qubit_distillation.ipynb      # Numerical investigation of N-qubit GHZ distillation
```

## Scalability and runtime constraints:

The memory and runtime requirements grow rapidly with the number of qubits.
In practice, the notebook "n_qubit_distillation.ipynb" constructs dense $2N$-qubit matrices whose memory scales as $O(16^N)$ and runtime as $O(64^N)$. On a 16 GB computer, $N=6$ is computationally expensive, while $N\geq7$ may cause excessive swapping, long runtimes, or out-of-memory failures. Use small $N$, avoid repeated trajectory recomputation, and prefer sparse or reduced-state implementations for larger systems.

For $N>=6$ run the memory-efficient version of the alternating protocol.

## Requirements

- Wolfram Mathematica       # version number 13.3.1.0
- Python                    # version number 3.14.4
- Jupyter Notebook
- NumPy
- SciPy
- Matplotlib

## Citation

If you use this repository or its results, please cite the associated article:

```bibtex
@article{rozgonyi2025practical,
  title   = {Practical scheme for efficient distillation of GHZ states},
  author  = {Rozgonyi, {\\'A}ron and Sz{\\'e}chenyi, G{\\'a}bor and
             K{\\'a}lm{\\'a}n, Orsolya and Kiss, Tam{\\'a}s},
  year    = {2025},
  eprint  = {2501.12268},
  archivePrefix = {arXiv},
  primaryClass  = {quant-ph},
  doi     = {10.48550/arXiv.2501.12268}
}
```