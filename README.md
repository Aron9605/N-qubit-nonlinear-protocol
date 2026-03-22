# N-qubit-nonlinear-protocol

This project provides code and scripts that reproduce the key findings presented in the paper **'Rozgonyi, Á., Széchenyi, G., Kálmán, O. and Kiss, T., 2025. Practical scheme for efficient distillation of GHZ states'**. arXiv preprint  [arXiv:2501.12268.](https://doi.org/10.48550/arXiv.2501.12268)


## Overview

<p align="justify">
Generating Greenberger-Horne-Zeilinger (GHZ) states in a lab remains a challenge due to imperfect operations and noisy devices. Noise in imperfect quantum states can be mitigated through entanglement distillation, a critical component of quantum communication protocols. 
We present an efficient local operation and classical communication (LOCC) scheme for distilling GHZ states from tripartite systems affected by both coherent and incoherent errors. Our method utilizes an iterative process that applies a postselection-based non-linear transformation to enhance the entanglement of three-qubit states. The scheme remains practical by employing a limited set of straightforward unitary operations and projective measurements in the computational basis, resulting in subexponential convergence to a pure GHZ state, similarly to the recent scheme for two-qubit Bell states[2].
We systematically develop a double-iteration protocol by establishing a mathematical framework for the transformation processes, with particular emphasis on the role of unitary operations in correcting small arbitrary errors in the initial states. Most importantly, our scheme can probabilistically transform 4 input copies of noisy GHZ states into a single, almost-perfect GHZ state, eliminating noise to first order. We also analytically derive a corresponding no-go theorem by demonstrating that such a scheme is impossible if only 2 inputs are provided. 
Notably, our protocol corrects small arbitrary distortions in GHZ states, converging subexponentially to a pure GHZ state while maintaining operational simplicity, thereby supporting its feasibility for practical quantum computing applications.
  
Finally, our hardware-efficient design is implementable on recent quantum computers, as evidenced by the low number of qubits required and the few 1- and 2-qubit gates needed. We employ the IBM Qiskit quantum simulator to test the protocol's performance on actual quantum hardware.
</p>

*References*:

[1] Áron Rozgonyi, Gábor Széchenyi, Orsolya Kálmán, Tamás Kiss. “Training iterated protocols for distillation of GHZ states with variational quantum algorithms.” Physics Letters A

[2] Kálmán, O., Gábris, A., Jex, I., & Kiss, T. (2025, December). Universal, unambiguous concentration and distillation of Bell pairs. Physical Review Letters, 135(26), 260202. https://doi.org/10.1103/rcx1-w6j7


## Repository Structure

* notebooks/: Source code for implementing the quantum protocols.
* authors/: Lists people who are significant authors of the project.
* docs/: Documentation and references for understanding the theory and implementation details.
* citation/: Full citation details are available, if you use this code or mention its results, please cite it.

## Code availability:
* 3qubit_symbolic.nb Analytical Mathematica notebook for the 3-qubit GHZ distillation protocol, including unitary construction, no-go theorem derivation, and noise analysis.
* n_qubit_distillation.ipynb Jupyter notebook provides a numerical investigation of the N-qubit GHZ distillation protocol, analyzing its performance and convergence behavior.

## Scalability and runtime constraints:

* In practice, running the code for systems larger than N > 6 qubits can significantly increase runtime.

## Requirements

* Wolfram Mathematica
* Python
