# N-qubit-nonlinear-protocol

This project contains the Wolfram Mathematica notebook (*3qubit_analitics.nb*) and Python notebook (*Nqubit_numerics.py*) for the reproduction of essential results of the '*Title.*' article. [ref. [Physics Letters A](https://doi.org/10.1016/j.physleta.2024.129349
)]

The study has been submitted to a scientific journal; the corresponding authors are **Aron Rozgonyi**[1,2], **Gabor Szechenyi**[1,2], **Orsolya Kalman**[2] and **Tamas Kiss**[2].

*Affiliations*:

[1] Institute of Physics, [Eotvos Lorand University](https://www.elte.hu/en/), Budapest, Hungary

[2] Department for Quantum Optics and Quantum Information, [HUN-REN Wigner Research Centre for Physics](https://wigner.hu/en/news), Budapest, Hungary


## Abstract

<p align="justify">
Advances in quantum technology lead to the potential for communication between remote quantum devices. The building blocks of quantum communication are highly entangled quantum bits (qubits).  The procedure of entangling qubits to high order is a nontrivial task. A partially entangled qubit pair needs error correction to increase the magnitude of entanglement. Certain nonlinear protocols may be applied for entanglement distillation were introduced in [1] consisting of local operations and classical communication (LOCC). The iterative application of this class of nonlinear protocols leads to an enhancement of the entanglement.
The protocol contains an ensemble made up of two pairs of n-qubits in the same state. At the beginning of the procedure, the parties agree on which qubits are to be measured. Then only local unitary operations are performed by the parties on their qubits before measuring them. After the measurement via classical communication, they post-select the zero measurement outcome on both sides, otherwise discard them. The non-linearity is due to the generalized feedback realized by selection conditioned measurement. By iterated application of the protocol, the remaining qubits may eventually exhibit higher order entanglement.
Recently, quantum networks have been an area of intense research, driven by the desire to connect distant quantum chips. Consider many parties in a multipartite system. We investigate whether a uniform protocol, similar to the long-studied bipartite case, can be designed for an n-qubit scenario. 
We introduce the alternating double iteration protocol, characterized by the sequential application of distinct unitary operators during its iterative steps. Specifically, the employment of  certain single and two-qubit (CNOT-X and CNOT-H) operators enables this protocol to effectively mitigate errors at a linear order. Furthermore, we demonstrate the sub-exponential improvement in noise within an alternating GHZ distillation protocol. The selection of the two-qubit gates enables the successful purification of marginally noisy GHZ states. Additionally, we conduct a comprehensive analysis of the protocol's performance in the presence of imperfect components, including noisy two-qubit gates and measurements. 
Finally, our hardware-efficient design is implementable on recent quantum computers, as evidenced by the low number of qubits required and the few 1- and 2-qubit gates needed. We employ the IBM Qiskit quantum simulator to test the protocol's performance on actual quantum hardware.
</p>

*References*:

[1] Alber, Gernot, Aldo Delgado, Nicolas Gisin, and Igor Jex. "Efficient bipartite quantum state purification in arbitrary dimensional Hilbert spaces." Journal of Physics A: Mathematical and General 34, no. 42 (2001): 8821.
[2] Áron Rozgonyi, Gábor Széchenyi, Orsolya Kálmán, Tamás Kiss. “Training iterated protocols for distillation of GHZ states with variational quantum algorithms.” Physics Letters A

## Code availability:
* 3qubit_analitics.nb Wolfram Mathematica notebook contains the analitical investigation of 3-qubit distillation and preparing the unitary operators.
* Nqubit_numerics.py Python notebook contains the numerical analysis of the N-qubit algorithm.
