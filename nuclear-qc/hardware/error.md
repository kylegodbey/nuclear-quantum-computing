<!-- #region -->
# Error Mitigation: Zero-Noise Extrapolation

Author: Alexandra Semposki

We know that, when running quantum circuits on a real quantum device, there will be some noise in our system (this is an example of fault-tolerance, a theory that claims there will always be such noise in quantum hardware). However, can we __quantify__ how much effect this noise produces in our circuit? Yes, we can! One method to do this is to use zero-noise extrapolation, or ZNE. 


## How it works

ZNE makes corrections to the expectation values of some observable calculated using quantum circuits. (In the VQE chapter, this will be the expectation value of the Hamiltonian to find the ground state energy of the atomic system in question.) To make these corrections properly, we can use knowledge of some underlying noise structure, or we can apply this technique without this knowledge. ZNE is able to handle either case well. 

Let's first take a look at the basic theory. We start with the expectation value $E$ of some observable that was measured in a noisy system. We can then expand this in a power series with respect to a noise parameter $\lambda$ around the zero-noise value we will call $E_{0}$:

$$
E(\lambda) \simeq E_{0} + \sum_{k=1}^{n} a_{k}\lambda^{k} + \cal{O}(\lambda^{n+1}),
$$

where $a_{k}$ are noise model-dependent coefficients, and $\lambda$ is the noise parameter \[1\]. If we can, instead of decreasing the noise down to zero, increase it by $n$ increments $\hat{E}(c_{i}\lambda)$, we can write a better estimate for the noiseless expectation value as 

$$
\hat{E}^{n}(\lambda) = \sum_{i=0}^{n} \gamma_{i}\hat{E}(c_{i}\lambda),
$$

(where $\gamma_{i}$ are solutions to conditions $\sum_{i} \gamma_{i} = 0$ and $\sum_{i} \gamma_{i}c_{i}^{k} = 0$ for each $k = 1,...n$) and fit these $n$ data points with a linear or exponential curve (depending on the shape of the points we get) and extrapolate to the zero-noise limit  \[1, 2\]. This is a very similar approach to extrapolating from a finite temperature backwards to a zero-temperature limit, or extrapolating to $q^{2} = 0$ in nuclear physics applications. 


## Looking ahead

In the next chapter on the Variational Quantum Eigensolver (VQE), we'll see ZNE applied to the $N=2,3$ cases of the ground state energy of the deuteron using the module for ZNE in the <tt>mitiq</tt> package, both for a simulator backend with a noise model, and a real IBM quantum device. 


## References  

- \[1\] Kandala, A., Temme, K., Córcoles, A.D. et al. Error mitigation extends the computational reach of a noisy quantum processor. Nature 567, 491–495 (2019) ([click here for a direct link](https://doi.org/10.1038/s41586-019-1040-7)).

- \[2\] <tt>mitiq</tt> documentation, "About Error Mitigation," 2020. (Page found [here](https://mitiq.readthedocs.io/en/v.0.1a2/guide/guide_06-error-mitigation.html)).
<!-- #endregion -->
