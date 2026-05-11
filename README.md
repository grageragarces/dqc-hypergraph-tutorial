# dqc-hypergraph-tutorial

Hands-on introduction to hypergraph representations of quantum circuits for distributed quantum computing (DQC).

## What's inside

A Jupyter notebook walking through three ways to model a quantum circuit as a hypergraph:

| Representation | Vertices | Hyperedges | Communication |
|---|---|---|---|
| **Telegate** | Qubits | Gates | Non-local gate execution |
| **Teledata** | Gates | Qubits | Qubit-state teleportation |
| **HDH** | Qubit-state moments | Gates | Quantum + classical, typed |

## Requirements

```bash
pip install qiskit[visualization] matplotlib hdh
```

## Usage

Open `hypergraph_representations.ipynb` (full version with diagrams) or
`hypergraph_representations_simple.ipynb` (outputs only).

Set `N = 1` in the configuration cell to choose how many circuits to demo,
and point `CIRCUITS_DIR` at a folder of OpenQASM 2.0 files.

## Background

The HDH representation is generated using the [`hdh`](https://github.com/grageragarces/HDH) library,
which outputs directed typed hypergraphs with metadata distinguishing classical
from quantum operations.
