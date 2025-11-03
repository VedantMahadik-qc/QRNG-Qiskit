# Quantum Random Number Generator (QRNG) with Qiskit

This project demonstrates the creation of a true random number generator using the principles of quantum mechanics. It is built with Qiskit and executed on IBM Quantum simulators.

## 1. Objective
The goal is to leverage quantum superposition to generate a sequence of truly random bits. A classical random number generator is pseudorandom, but a QRNG is probabilistic by nature.

This is achieved with a simple 1-qubit circuit:
1.  Apply a **Hadamard (H) gate** to put the qubit in an equal superposition of $|0\rangle$ and $|1\rangle$.
2.  **Measure** the qubit. The result will be 0 or 1 with a 50% probability, a fundamentally random outcome.
3.  Repeat this process (shots) to generate a sequence of random bits.

## 2. Technologies Used
* **Python**
* **Qiskit**
* **NumPy**
* **Matplotlib**

## 3. How to Run
1.  Clone the repository.
2.  Install the required libraries: `pip install -r requirements.txt`
3.  Open and run the `.ipynb` notebook in a Jupyter environment.

## 4. Key Results
The notebook executes the circuit on an IBM Quantum simulator and plots a histogram of the results, demonstrating the (near) 50/50 probability distribution of 0s and 1s, confirming the randomness of the generator.
