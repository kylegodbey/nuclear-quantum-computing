# Conclusions and Acknowledgements

Through this jupyter book we have gone through various fundamental concepts and tools needed for implementing nuclear model calculations on quantum computers. We explained and developed the Variational Quantum Eigensolver in the first chapter, showcasing an implementation of the deuteron with additional improvements for speeding convergence. In chapter two we went through the intrinsic noise associated with quantum circuits, and addressed ways of dealing with it through the Zero Noise Extrapolation algorithm. In chapter three we explored the Reduced Basis Method, a dimensionality reduction technique capable of transforming problems involving thousands of degrees of freedom into just a few interacting "quasi particles". This is a crucial step into translating calculations for quantum computers with access to just few qbits. Finally, in the last chapter we added everything together to tackle the Gross-Pitaevskii equation, a simple model for describing dilute Bose-Einstein condensates. 

With all these tools in place you, the reader, have now the possibility to implement your own calculations into a quantum computer. Following a similar flowchart as the one we developed in the last chapter you should find a reduced order model for your system (perhaps using the reduced basis method), which could then be implemented into a quantum circuit for using the Variational Quantum Eigensolver algorithm. Don't forget to use also some noise mitigation technique such as the Zero Noise Extrapolation if you are dealing with a noisy circuit. Let us know through our contact person Kyle Godbey on your success in this journey!

We will like to thank the organizers of the 2022 FRIB Theory Alliance Summer School on Quantum Computing and Nuclear Few- and Many-Body Problems for the incredible opportunity of learning about all these topics from world experts, as well as for raising a "final challenge" that lead to the construction of this jupyter book. 

In particular, we would like to thank:

Ben Hall and Morten Hjorth-Jensen for a fantastic explanation of the Variational Quantum Eigensolver
Ryan Larose for another fantastic explanation on the Zero Noise Extrapolation algorithm
Dean Lee for great discussions about the Gross-Pitaevskii
