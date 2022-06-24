<!-- #region -->
# Introduction

 - TODO: Primary motivations and intent of current work, along with motivating statements of QC in general
 
 
 - Many of the most intriguing problems known by the physics community are presently unreachable by classical computation 
 
     - Diagonalization of high-dimensional matrices cannot be performed beyond a dimension of $10^{11}$ currently (see Tsunoda, N., Otsuka, T., Takayanagi, K. et al. The impact of nuclear shape on the emergence of the neutron dripline. Nature 587, 66–71 (2020).     
         
     - The fermion sign problem pervades Quantum Monte Carlo (QMC) calculations


 - Our hope is that, in the near future (with the fast developments in the quantum computing (QC) world), we may be able to mitigate these issues with quantum computers that will reduce our time to compute more computationally challenging physics problems from exponential time to polynomial time
 
 - Error correction and mitigation are also fast advancing (add some info here)
  
 - A technique that has been used quite often in QC is the Variational Quantum Eigensolver (VQE), which can determine the ground state of some atomic system. It is very popular in Quantum Chemistry and there have been many applications of it in recent years (for example, [this PRL paper from 2018](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.120.210501). (insert more about VQE but not too much here)
 
     - In this Jupyter Book, we will use the example of the pionless-EFT Hamiltonian for the deuteron from this paper and perform VQE to find the ground state energy as a benchmark in our understanding of this QC method. We start by using VQE on $N=2$, where $N$ is the number of dimensions, and then progress to $N=3$. After this, we extend this work to a general case where we are able to ask for any dimension we would like to calculate. 
     
     - As we wish to investigate VQE on more than just the deuteron, we will then discuss the Reduced Basis Method (RBM) in the context of the (insert Hamiltonian here), as we need to reduce the dimensionality of this Hamiltonian to one that can be handled by our available IBM quantum computers. We then perform VQE on this reduced Hamiltonian, and test this on a real quantum device. Since these qubits will have error, we will attempt error correction to mitigate any bit or phase flips that may occur in our circuit. 
<!-- #endregion -->

```python

```
