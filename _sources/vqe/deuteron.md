# Quantum Computing the Deuteron

Author: Jingyi Li

In this introduction we will briefly discuss the 2018 paper, [Cloud Quantum Computing of an Atomic Nucleus](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.120.210501).

From the paper we can read that the authors employed the projection of hamiltonian operators onto quantum qubits (X,Y,Z) to construct a quantum computatable hamiltonian by the Pionless EFT, a systematically improvable and model-independent approach to nuclear interactions in a regime where the momentum scale $Q$ of the interesting physics. The important part of this paper is how the deuteron creation and annihilation operator is mapped onto qubits using Jordan-Wigner transformation. Qubits can be used by quantum computers for operations based on Pauli matrices (denoted as $X_{q}, Y_{q}$, and $Z_{q}$ on qubit $q$ ).

## Defining the Hamiltonian

The deuteron Hamiltonian is 
\begin{equation}
H_{N}=\sum_{n, n^{\prime}=0}^{N-1}\left\langle n^{\prime}|(T+V)| n\right\rangle a_{n^{\prime}}^{\dagger} a_{n} .
\end{equation}

The operators $a_{n}^{\dagger}$ and $a_{n}$ here are the creation and annihilation operators. A deuteron is created or annihilated in the harmonic-oscillator $s$-wave state $|n\rangle$. The matrix elements of the kinetic and potential energy are represented by:
\begin{equation}
\begin{aligned}
\left\langle n^{\prime}|T| n\right\rangle=& \frac{\hbar \omega}{2}\left[(2 n+3 / 2) \delta_{n}^{n^{\prime}}-\sqrt{n(n+1 / 2)} \delta_{n}^{n^{\prime}+1}\right.\\
&\left.-\sqrt{(n+1)(n+3 / 2)} \delta_{n}^{n^{\prime}-1}\right] \\
\left\langle n^{\prime}|V| n\right\rangle=& V_{0} \delta_{n}^{0} \delta_{n}^{n^{\prime}}
\end{aligned}
\end{equation}

Here, $V_{0}=-5.68658111 \mathrm{MeV}$, and $n, n^{\prime}=0,1, \ldots N-1$, for a basis of dimension $N$. We also set $\hbar \omega=7 \mathrm{MeV}$.

## Mapping the deuteron onto qubits

Quantum computers manipulate qubits by operations based on Pauli matrices (denoted as $X_{q}, Y_{q}$, and $Z_{q}$ on qubit $q$ ). The deuteron creation and annihilation operators can be mapped onto Pauli matrices via the Jordan-Wigner transformation, defined as,

\begin{equation}
\begin{aligned}
&a_{n}^{\dagger} \rightarrow \frac{1}{2}\left[\prod_{j=0}^{n-1}-Z_{j}\right]\left(X_{n}-i Y_{n}\right) \\
&a_{n} \rightarrow \frac{1}{2}\left[\prod_{j=0}^{n-1}-Z_{j}\right]\left(X_{n}+i Y_{n}\right) .
\end{aligned}
\end{equation}

Note that other mappings can be used, with the various mappings having benefits and drawbacks that may apply to your problem of interest.

A spin up $|\uparrow\rangle$ (down $|\downarrow\rangle$ ) on qubit $n$ corresponds to zero (one) deuteron in the state $|n\rangle$. For $N=2,3$ we have the components of the Hamiltonian (all numbers are in units of $\mathrm{MeV}$)

\begin{equation}
\begin{aligned}
H_{2}=& 5.906709 I+0.218291 Z_{0}-6.125 Z_{1} \\
&-2.143304\left(X_{0} X_{1}+Y_{0} Y_{1}\right)
\end{aligned}
\end{equation}

\begin{equation}
H_{3}=H_{2}+9.625\left(I-Z_{2}\right)-3.913119\left(X_{1} X_{2}+Y_{1} Y_{2}\right)
\end{equation}
