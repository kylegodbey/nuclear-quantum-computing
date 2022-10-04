# Conclusions and Acknowledgements

Through this Jupyter book we have gone through various fundamental concepts and tools needed for implementing nuclear model calculations on quantum computers. We explained and developed the Variational Quantum Eigensolver in the first chapter, showcasing an implementation of the deuteron with additional improvements for speeding convergence. In chapter two we went through the intrinsic noise associated with quantum circuits, and addressed ways of dealing with it through the Zero-Noise Extrapolation algorithm. In chapter three we explored the Reduced Basis Method, a dimensionality reduction technique capable of transforming problems involving thousands of degrees of freedom into just a few interacting "quasiparticles". This is a crucial step into translating calculations for quantum computers with access to just few qubits. Finally, in the last chapter we added everything together to tackle the Gross-Pitaevskii equation, a simple nonlinear model for describing dilute Bose-Einstein condensates. 

With all these tools in place, you, the reader, now have the ability to implement your own calculations onto a quantum computer. Following a similar workflow as the one we developed in the last chapter, you could find a reduced order model for your system (perhaps using the reduced basis method), which could then be mapped onto a quantum circuit for use with the Variational Quantum Eigensolver algorithm. Don't forget to also use some noise mitigation technique such as the Zero Noise Extrapolation if you are dealing with a noisy circuit. Be sure to let us know if you apply anything you've learned from this book to your own problems of interest and share your successes on this journey! If you'd like, we could even explore adding it to the book - so send any comments or questions to Kyle via <qc@kyle.ee>.

We will like to thank all of the organizers of the 2022 FRIB Theory Alliance Summer School on Quantum Computing and Nuclear Few- and Many-Body Problems for the incredible opportunity of learning about all these topics from world experts, as well as for raising a "final challenge" that lead to the construction of this Jupyter book. 

For the topics found in this book in particular, we would like to thank:

- Ben Hall and Morten Hjorth-Jensen for a fantastic explanation of the Variational Quantum Eigensolver
- Ryan Larose for another fantastic explanation on the Zero Noise Extrapolation algorithm
- Dean Lee for great discussions about the Gross-Pitaevskii equation

```{figure} ice.jpg
---
height: 150px
name: ice-fig
---
Celebratory ice cream the day after the summer school!
```
