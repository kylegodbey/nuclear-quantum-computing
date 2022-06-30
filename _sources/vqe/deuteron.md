# Quantum Computing the Deuteron

TODO: Discuss 2018 paper [Cloud Quantum Computing of an Atomic Nucleus](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.120.210501), discuss the deuteron and the model maybe? It should be somewhere, maybe here instead of the notebook. Just need a light introduction before the real work.

The deuteron model from the paper 2018 is motivated by the current quantum computer situation

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

Here, $V_{0}=-5.68658111 \mathrm{MeV}$, and $n, n^{\prime}=0,1, \ldots N-1$, for a basis of dimension $N$. We set $\hbar \omega=7 \mathrm{MeV}$, and the potential has an ultraviolet cutoff $\Lambda \approx 152 \mathrm{MeV}$ [28], which is still well separated from the bound-state momentum of about $Q \approx 46 \mathrm{MeV}$.

Mapping the deuteron onto qubits.-Quantum computers manipulate qubits by operations based on Pauli matrices (denoted as $X_{q}, Y_{q}$, and $Z_{q}$ on qubit $q$ ). The deuteron creation and annihilation operators can be mapped onto Pauli matrices via the Jordan-Wigner transformation

\begin{equation}
\begin{aligned}
&a_{n}^{\dagger} \rightarrow \frac{1}{2}\left[\prod_{j=0}^{n-1}-Z_{j}\right]\left(X_{n}-i Y_{n}\right) \\
&a_{n} \rightarrow \frac{1}{2}\left[\prod_{j=0}^{n-1}-Z_{j}\right]\left(X_{n}+i Y_{n}\right) .
\end{aligned}
\end{equation}

A spin up $|\uparrow\rangle$ (down $|\downarrow\rangle$ ) on qubit $n$ corresponds to zero (one) deuteron in the state $|n\rangle$. As we deal with single-particle states, the symmetry under permutations plays no role here. To compute the ground-state energy of the deuteron we employ the following strategy. We determine the ground-state energies of the Hamiltonian (1) for $N=1,2,3$ and use those values to extrapolate the energy to the infinite-dimensional space. We have $H_{1}=0.218291\left(Z_{0}-I\right) \mathrm{MeV}$, and its ground-state energy $E_{1}=\left\langle\downarrow\left|H_{1}\right| \downarrow\right\rangle \approx-0.436 \mathrm{MeV}$ requires no computation. Here, $I$ denotes the identity operation. For $N=2,3$ we have (all numbers are in units of $\mathrm{MeV}$ )

\begin{equation}
\begin{aligned}
H_{2}=& 5.906709 I+0.218291 Z_{0}-6.125 Z_{1} \\
&-2.143304\left(X_{0} X_{1}+Y_{0} Y_{1}\right)
\end{aligned}
\end{equation}


\begin{equation}
H_{3}=H_{2}+9.625\left(I-Z_{2}\right)-3.913119\left(X_{1} X_{2}+Y_{1} Y_{2}\right)
\end{equation}

We note that the tridiagonal structure of our Hamiltonian can be implemented efficiently on a linear chain of connected qubits and this suits existing designs. The simulation of the Hamiltonian $H_{N}$ requires $N-1$ angles and the circuit depth is linear in $N$.

For the extrapolation to the infinite space we employ the harmonic-oscillator variant of Lüscher's formula [29] for finite-size corrections to the ground-state energy [30]

\begin{equation}
\begin{aligned}
E_{N}=&-\frac{\hbar^{2} k^{2}}{2 m}\left(1-2 \frac{\gamma^{2}}{k} e^{-2 k L}-4 \frac{\gamma^{4} L}{k} e^{-4 k L}\right) \\
&+\frac{\hbar^{2} k \gamma^{2}}{m}\left(1-\frac{\gamma^{2}}{k}-\frac{\gamma^{4}}{4 k^{2}}+2 w_{2} k \gamma^{4}\right) e^{-4 k L} .
\end{aligned}
\end{equation}

Here, the finite-basis result $E_{N}$ equals the infinite-basis energy $E_{\infty}=-\hbar^{2} k^{2} /(2 m)$ plus exponentially small corrections. In Eq. (6), L=L $L N)$ is the effective hardwall radius for the finite basis of dimension $N, k$ is the bound-state momentum, $\gamma$ the asymptotic normalization coefficient, and $w_{2}$ an effective range parameter. For $N=1,2$, and 3 we have $L(N)=9.14,11.45$, and $13.38 \mathrm{fm}$ as the effective hard-wall radius in the oscillator basis with $\hbar \omega=7 \mathrm{MeV}$, respectively, and $L(N) \approx$ $\sqrt{(4 N+7) \hbar /(m \omega)}$ for $N \gg 1[31]$. Using the groundstate energies $E_{N}$ for $N=1,2$ allows one to fit the leading $O\left(e^{-2 k L}\right)$ and subleading $O\left(k L e^{-4 k L}\right)$ corrections by adjusting $k$ and $\gamma$. Inclusion of the $N=3$ ground-state energy also allows one to fit the smaller $O\left(e^{-4 k L}\right)$ correction by adjusting $w_{2}$. The results of this extrapolation are presented in the upper part of Table I, together with the energies $E_{N}$ from matrix diagonalization. We note that the most precise $N=2(N=3)$ extrapolated result is about $2 \%(0.5 \%)$ away from the deuteron's ground-state energy of $-2.22 \mathrm{MeV}$.


$\begin{aligned} U(\theta) & \equiv e^{\theta\left(a_{0}^{\dagger} a_{1}-a_{1}^{\dagger} a_{0}\right)}=e^{i(\theta / 2)\left(X_{0} Y_{1}-X_{1} Y_{0}\right)} \\ U(\eta, \theta) & \equiv e^{\eta\left(a_{0}^{\dagger} a_{1}-a_{1}^{\dagger} a_{0}\right)+\theta\left(a_{0}^{\dagger} a_{2}-a_{2}^{\dagger} a_{0}\right)} \\ & \approx e^{i(\eta / 2)\left(X_{0} Y_{1}-X_{1} Y_{0}\right)} e^{i(\theta / 2)\left(X_{0} Z_{1} Y_{2}-X_{2} Z_{1} Y_{0}\right)} \end{aligned}$

For generating the hamiltonian, we need a wire(qubit) that define the rotation $e^{i\theta}$ and two other qubit to define the Pauli matrix $X_{0},X_{1}$ and $Y_{0},Y_{1}$.
