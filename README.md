Quantum Random Number Generator (QRNG) with Qiskit

This Jupyter Notebook (Qrng Trial.ipynb) demonstrates how to build and analyze a simple Quantum Random Number Generator (QRNG) using the Qiskit AerSimulator. It explores the principles of quantum superposition and measurement to generate truly random bits and then runs statistical tests to check their quality.

Notebook Contents

The notebook is divided into several parts:

Part 1: Simulating the QRNG in Bulk
Creates a basic 1-qubit circuit (Hadamard gate + Measure) and runs it 1024 times to show the 50/50 probability distribution.

Part 2: Generating a Random Bit Sequence
Runs the same 1-qubit circuit one shot at a time to build a list of sequential random bits.

Part 3: Analyzing the Random Bits

Generates a large sample (10,000 bits) for analysis.

Performs several statistical randomness tests:

Shannon Entropy (ideally 1.0)

Chi-Square Test (checking for bias)

Runs Test (checking for patterns)

Compares the distribution and entropy of the quantum-generated bits to a classical pseudo-random number generator (from NumPy).

Part 4: Generating Bits in Parallel
Shows a more efficient method using a 4-qubit circuit to generate four random bits per shot.

Part 5: Applications of QRNG
Demonstrates two simple applications for the generated random bits:

XOR Encryption: A basic implementation of a one-time pad cipher.

Monte Carlo Pi Estimation: Uses random (x, y) coordinates to estimate the value of Pi.

Setup & Installation

To run this notebook, you will need a Python environment with Jupyter and the Qiskit libraries.

Recommended: Create a Conda Environment
It is highly recommended to use a clean Conda environment to avoid package conflicts.

conda create -n qiskit-env python=3.10
conda activate qiskit-env


Install Dependencies
This notebook requires the following Python packages. You can install them using pip:

# Install Qiskit's core and simulator
pip install qiskit
pip install qiskit-aer

# Install libraries for analysis and plotting
pip install matplotlib
pip install scipy

# Install jupyter to run the notebook
pip install jupyterlab


Running the Notebook

From your terminal (with the qiskit-env activated), run:

jupyter lab


This will open JupyterLab in your browser.

Open the Qrng Trial.ipynb file.

You can run the cells one by one (using Shift + Enter) or run all cells by clicking Run > Run All Cells.
