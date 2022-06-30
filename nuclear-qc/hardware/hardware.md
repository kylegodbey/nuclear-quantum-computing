# Running on "Hardware"

Author: Alexandra Semposki

In the last chapter, we extensively discussed the VQE method and showed its results on a simulator. However, we did not explain much about that simulator---what is a quantum simulator in comparison to a real quantum computer? What differences arise between the two, and what issues can one run into using the two devices? 

A __quantum simulator__, such as the `qiskit.Aer` simulator, is a device that mimics a real quantum computer, but in the sense that it computes everything the way a quantum computer would do, *except* it acts as if the device has no noise. This is not realistic because it is known that real quantum devices will have noise in their circuits (a full explanation of sources and effects of noise in a real quantum device is given on the next page). 

A __real quantum computer__, such as the IBM quantum machines available for use through <tt>Qiskit</tt>, have a limited number of qubits to use, and these qubits all have errors come up when running quantum circuits with them. Quantum simulators generally have many more qubits available for use, but do tend to only be able to accurately calculate up to a few dozen qubits. 

The quantum simulator is very useful for testing out a quantum circuit or full code before sending it to a real quantum computer and waiting for your turn in the queue. Since the IBM quantum computers available are a limited number, there can be long job queues until your circuit is run, so double-checking your work on a simulator first is always a good idea. But what about when you get your results back from the quantum computer and you see you have errors in your results from the real devices? What then? On the next page, and in much of this chapter, we will be exploring different kinds of error correction and mitigation, and trying out an error mitigation technique on the $N=2$ case of the deuteron from the last chapter to see how the world of errors works in quantum computing. 