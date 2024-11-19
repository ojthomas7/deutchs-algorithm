# Deutch's Algorithm

## Overview

This repository uses IBM's quantum composer and the Qiskit SDK to implement Deutch's algorithm, one of the first demonstrations that quantum computation could be faster than classical at solving certain problems. Here, I build and explain a quantum circuit that demonstrates this algorithm.

## The Circuit:

<p align="center">
  <img src="deutch.jpeg" alt="Image 1" width="600"/>
</p>
<p align = "center">
<i>Quantum teleportation circuit, created with IBM composer and the Qiskit SDK. An arbitrary qubit interacts with an entangled Bell state via a CNOT followed by a Hadamard gate. Measurements are made of the arbitrary qubit and one half of the EPR pair, and the relavant transformations are made to the second half of the EPR pair depending on the results of this measurement.</i>
</p> 

## The Algorithm:

Consider a case where we want to determine wether a function is constant. We have a binary function:

$$f: [0, 1] \to [0, 1]$$

Which takes an input of euther 0 or 1 and returns either 0 or 1.

If this function were balanced, it would have as many outputs for 0 as it did for 1, and if it were constant it would either output only 0 or only 1. A classical computer would need two queries to this function to determine wether $f(0) = f(1)$ amd that the function is therefore constant, whilst a quantum computer would require a single query.

This is done by implementing a reversible oracle function - essentially a 'black-box' - which takes an input, performs a specific operation, and returns an output.
