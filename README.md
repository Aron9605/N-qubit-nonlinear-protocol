# N-qubit-nonlinear-protocol

This project contains the Wolfram Mathematica notebook (*3qubit_analitics.nb*) and Python notebook (*Nqubit_numerics.py*) for the reproduction of essential results of the project '*Practical scheme for efficient distillation of GHZ states*' . [ref.]

The study has been submitted to a scientific journal; the corresponding authors are **Aron Rozgonyi**[1,2,3,4], **Gabor Szechenyi**[1,2], **Orsolya Kalman**[2] and **Tamas Kiss**[2].

*Affiliations*:

[1] Institute of Physics, [Eotvos Lorand University](https://www.elte.hu/en/), Budapest, Hungary

[2] Department for Quantum Optics and Quantum Information, [HUN-REN Wigner Research Centre for Physics](https://wigner.hu/en/news), Budapest, Hungary

[3] PQI - Portuguese Quantum Institute, Lisbon, Portugal

[4] Physics of Information and Quantum Technologies Group, Centro de Física e Engenharia de Materiais Avançados (CeFEMA), Lisbon, Portugal

## Abstract

<p align="justify">
We develop an efficient local operation and classical communication (LOCC) scheme for the distillation of Greenberger-Horne-Zeilinger (GHZ) states from tripartite systems subjected to both coherent and incoherent errors. The proposed method employs an iterative process that employs a postselection based non-linear transformation to increase the entanglement of 3-qubit states. In contrast to traditional distillation protocols that require an exponential number of initial states as a resource, our method achieves subexponential convergence towards a pure GHZ state. The proposed scheme practical in the sense that it employs a small set of relatively simple unitary operations and projective measurements in the computational basis.
We systematically develop a double-iteration protocol by providing a mathematical framework for the transformation processes involved, emphasizing the role of unitary operations in correcting arbitrary small errors in the initial states. Through analytical derivations and numerical simulations, we demonstrate the protocol's ability to progressively eliminate noise and improve fidelity over subsequent iterations.
Significantly, our protocol not only corrects for small arbitrary distortions in the GHZ states, but also maintains operational simplicity, making it feasible for practical quantum computing applications. 
  
Finally, our hardware-efficient design is implementable on recent quantum computers, as evidenced by the low number of qubits required and the few 1- and 2-qubit gates needed. We employ the IBM Qiskit quantum simulator to test the protocol's performance on actual quantum hardware.
</p>

*References*:

[1] Áron Rozgonyi, Gábor Széchenyi, Orsolya Kálmán, Tamás Kiss. “Training iterated protocols for distillation of GHZ states with variational quantum algorithms.” Physics Letters A

## Code availability:
* 3qubit_analitics.nb Wolfram Mathematica notebook contains the analitical investigation of 3-qubit distillation and preparing the unitary operators.
* Nqubit_numerics.py Python notebook contains the numerical analysis of the N-qubit algorithm.
