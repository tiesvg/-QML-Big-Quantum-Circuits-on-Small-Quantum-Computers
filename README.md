# Big Quantum Circuits on Small Quantum Computers

An implementation of a parametrized quantum circuit (PQC) as a binary classifier, paired with an exploration of how to reproduce the output of a larger m-qubit circuit using many runs of a smaller k-qubit circuit.

## Background

Near-term quantum hardware has a limited number of qubits, which caps the size of circuits that can actually be executed. Circuit cutting techniques try to close this gap by replicating the behaviour of a large circuit using a collection of smaller ones whose outputs are classically recombined. This project first builds a working PQC classifier, then asks how faithfully — and at what cost in number of circuits — a smaller PQC can stand in for a larger one.

## What's in here

- A PQC binary classifier with ansatz `U(x, θ) = U_train(θ) U_enc(x)`, trained on a benchmark dataset and validated with cross-validation.
- An implementation that replicates the output of an m-qubit ansatz using many instances of a smaller k-qubit ansatz, plus tests of how well the reconstruction generalizes.
- Experiments on how the number of small circuits required scales as the gap between m and k grows.
