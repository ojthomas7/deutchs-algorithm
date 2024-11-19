# Deutch's Algorithm

## Overview

This repository uses IBM's quantum composer and the Qiskit SDK to implement Deutch's algorithm, one of the first demonstrations that quantum computation could be faster than classical at solving certain problems. Here, I build and explain a quantum circuit that demonstrates this algorithm.

## The Circuit:

<p align="center">
  <img src="teleportation.jpeg" alt="Image 1" width="600"/>
</p>
<p align = "center">
<i>Quantum teleportation circuit, created with IBM composer and the Qiskit SDK. An arbitrary qubit interacts with an entangled Bell state via a CNOT followed by a Hadamard gate. Measurements are made of the arbitrary qubit and one half of the EPR pair, and the relavant transformations are made to the second half of the EPR pair depending on the results of this measurement.</i>
</p> 

## The Algorithm:

Consider a case where we want to determine wether a function is constant. We have a function:

$$f:{0, 1} \to {0, 1}$$
