# Variational Quantum Eigensolver

Author: Alexandra Semposki

The variational quantum eigensolver (VQE) has been used prominently in QC in the past few years as a way to find the ground state energy of a system. This is done using the variational method from quantum mechanics, which is able to provide an upper bound for this ground state energy. We start with a Hermitian Hamiltonian, $H$, and write the eigenvalue equation down as

$$
H | \psi_{i} \rangle = \lambda_{i} | \psi_{i} \rangle.
$$

Say, however, that we cannot directly solve this and must instead use states $| \psi(\theta) \rangle$, which have some variable angle $\theta$ dependence, and can be expanded in a basis of the original states such that

$$
| \psi(\theta) \rangle = \sum_{i} c_{i} | \psi_{i} \rangle.
$$

Now we can find the expectation value.

$$
\langle \psi(\theta) | H | \psi(\theta) \rangle = \sum_{i,j} c_{j}^{*} c_{i} \langle \psi_{j} | H | \psi_{i} \rangle = \sum_{i,j} \delta_{ij} c_{j}^{*} c_{i} E_{i},
$$

and finally 

$$
\langle \psi(\theta) | H | \psi(\theta) \rangle = \sum_{i} |c_{i}|^{2} E_{i},
$$

and we know that 

$$
\langle \psi(\theta) | H | \psi(\theta) \rangle = E \ge E_{0},
$$

so we can minimize the angles $\theta$ and get

$$
\textrm{min} \langle \psi(\theta) | H | \psi(\theta) \rangle = E_{0}.
$$

VQE will attempt to do this angle minimization to obtain a reasonable approximation to the ground state energy of the deuteron in this chapter. (To see the notebook this was adapted from, and an excellent tutorial using a very simple Hamiltonian, click [here](https://github.com/NuclearPhysicsWorkshops/FRIB-TASummerSchoolQuantumComputing/blob/main/doc/pub/lecture7/ipynb/lecture7.ipynb)).

When it comes to implementing this technique, there are a few main ingredients in the recipe:

1. The Hamiltonian in question transformed into the Pauli basis using the __Jordan-Wigner transformation__;

2. A suitable __ansatz__ for the wave function;

3. A classical __optimization routine__ to be used to continously optimize the angles $\theta$ for each run of the VQE circuit. 

In the next chapter, we will see these three ingredients worked out in detail and implemented using the package <tt>pennylane</tt>.
