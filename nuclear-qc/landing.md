# Quantum Computing Applications in Nuclear Physics

This book of background, tutorials, and applications of aspects of quantum computing was born out of the [2022 FRIB quantum computing summer school](https://github.com/NuclearPhysicsWorkshops/FRIB-TASummerSchoolQuantumComputing) and attempts to explore tools and techniques of interest to nuclear physicists.

Through this virtual book, we will go through three main topic : 

1) The Variational Quantum Eigensolver, a technique that uses a hybrid approach between a classical and a quantum computer to calculate the ground state configuration of a system. We showcase the technique by applying it to the computation of the ground state of the deuteron.

2) The noise challenges that arise from running a non-idealized quantum circuit, including techniques for mitigation such as the Zero Noise Extrapolation. We will give an overview on the origins and structure of quantum noise, as well as present how it can be applied to the deuteron problem.

3) Dimensionality reduction techniques, in particular the Reduced Basis Method. These techniques could be crucial to reduce the (usually houndreds, thousands, or milliomns) effective degrees of freedom of a system to a point where it becomes accessible to modern few-qbits computers. In particular, we show how the Quantum Harmonic Oscillator in coordinate representation can be reduced to a two body system of interacting "particles" in the configuration space constructed by the reduced basis.

The tools we develop and showcase in these three topics will come to play together to tackle a challenging problem in the final part of this book: using a quantum computer we will solve the one dimensional Gross-Pitaevskii equation. This nonlinear Schrödinger equation approximately describes the low-energy properties of dilute Bose-Einstein condensates, and is one of the simplest models describing many-body quantum systems. We will use the Variational Quantum Eigensolver to find the ground state of the reduced system for different Hamiltonian parameters, while the Zero Noise Extrapolation will be exploited to produce accurate results even in the presence of noise.

A pdf version of this book can be downloaded [here](nuclear-qc.pdf).

List of contributors can be found [here](contributors.md).

```{tableofcontents}
```
