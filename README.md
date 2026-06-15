# Fermionic Matchgate QSVM

This repository contains a Quantum Machine Learning (QML) implementation of a Quantum Support Vector Machine (QSVM). It leverages custom Fermionic Matchgates built in [PennyLane](https://pennylane.ai/) to compute a quantum kernel, which is then used by a classical `scikit-learn` SVM for binary classification.

## Overview

The core of this project is a custom quantum feature map utilizing nearest-neighbor two-qubit interactions. The model is tested on a binary-classification subset of the classical Wine dataset.

### Key Features
* **Custom Matchgates:** Implementations of parameterized rotation matchgates (`MatchRyRy`, `MatchRzRz`) and entangling matchgates (`MatchZX`, `MatchHH`).
* **Efficient Kernel Estimation:** Uses PennyLane's `@qml.adjoint` decorator for highly efficient $U^\dagger(x) U(x)$ state overlap calculations.
* **Classical-Quantum Integration:** Seamlessly feeds the computed Quantum Kernel Matrix ($K$) into a `scikit-learn` Support Vector Classifier (`SVC`).

## Installation

To run this notebook, you will need Python 3.8+ and the following dependencies:
pennylane, numpy, scikit-learn, matplotlib

## Roadmap & Future Work

Convergence Rate Testing: (Work in Progress) Adding SWAP gates to evaluate the convergence rates of the QSVM.

