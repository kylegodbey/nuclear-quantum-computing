# Quantum Computing the Deuteron

TODO: Discuss 2018 paper [Cloud Quantum Computing of an Atomic Nucleus](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.120.210501), discuss the deuteron and the model maybe? It should be somewhere, maybe here instead of the notebook. Just need a light introduction before the real work.

From the paper we can read that the authors employed the projection of hamiltonian operators onto quantum qubits (X,Y,Z) to construct a quantum computatable hamiltonian.
By the Pionless EFT, a systematically improvable and model-independent approach to nuclear interactions in a regime where the momentum scale $Q$ of the interesting physics. The important part of this paper is how the deuteron creation and annihlation operator is mapped onto qubits using Jordan-Wigner transformation. Qubits can be used by quantum computers for boperations based on Pauli matrices (denoted as $X_{q}, Y_{q}$, and $Z_{q}$ on qubit $q$ ).

The deuteron Hamiltonian is 
\begin{equation}
H_{N}=\sum_{n, n^{\prime}=0}^{N-1}\left\langle n^{\prime}|(T+V)| n\right\rangle a_{n^{\prime}}^{\dagger} a_{n} .
\end{equation}

The operators $a_{n}^{\dagger}$ and $a_{n}$ here are the creatiion and annihilation operators. A deuteron is created or annihilated in the harmonic-oscillator $s$-wave state $|n\rangle$. The matrix elements of the kinetic and potential energy are represented by:
\begin{equation}
\begin{aligned}
\left\langle n^{\prime}|T| n\right\rangle=& \frac{\hbar \omega}{2}\left[(2 n+3 / 2) \delta_{n}^{n^{\prime}}-\sqrt{n(n+1 / 2)} \delta_{n}^{n^{\prime}+1}\right.\\
&\left.-\sqrt{(n+1)(n+3 / 2)} \delta_{n}^{n^{\prime}-1}\right] \\
\left\langle n^{\prime}|V| n\right\rangle=& V_{0} \delta_{n}^{0} \delta_{n}^{n^{\prime}}
\end{aligned}
\end{equation}


