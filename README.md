# Quantum Random Number Generator (QRNG) with Qiskit

This Jupyter Notebook (`Qrng Trial.ipynb`) demonstrates building and analyzing a simple Quantum Random Number Generator (QRNG) using the Qiskit AerSimulator. It explores the principles of quantum superposition and measurement to generate truly random bits and then runs statistical tests to check their quality.

##  Notebook Contents

The notebook is divided into several parts:

* **Part 1: Simulating the QRNG in Bulk**
Creates a basic 1-qubit circuit (Hadamard gate + Measure) and runs it 1024 times to show the 50/50 probability distribution.

* **Part 2: Generating a Random Bit Sequence**
Runs the same 1-qubit circuit one shot at a time to build a list of sequential random bits.

* **Part 3: Analyzing the Random Bits**
Generates a large sample (10,000 bits) for analysis and performs several statistical randomness tests:
    * **Shannon Entropy** (ideally 1.0)
    * **Chi-Square Test** (checking for bias)
    * **Runs Test** (checking for patterns)
It also compares the distribution and entropy of the quantum-generated bits to a classical pseudo-random number generator (from NumPy).

* **Part 4: Generating Bits in Parallel**
Shows a more efficient method using a 4-qubit circuit to generate four random bits per shot.

* **Part 5: Applications of QRNG**
Demonstrates two simple applications for the generated random bits:
    * **XOR Encryption:** A basic implementation of a one-time pad cipher.
    * **Monte Carlo Pi Estimation:** Uses random (x, y) coordinates to estimate the value of Pi.

---

## 🚀 Setup & Installation

To run this notebook, you will need a Python environment with Jupyter and the Qiskit libraries.

### 1. Recommended: Create a Conda Environment
It is highly recommended to use a clean Conda environment to avoid package conflicts.
*(This notebook was tested with `python=3.10`)*
```bash
conda create -n qiskit-env python=3.10
conda activate qiskit-env
