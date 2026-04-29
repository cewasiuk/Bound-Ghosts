# Bound Ghosts — Quantum Stability Without Runaway

**Companion code for:**
> *Ghost Degrees of Freedom Without Quantum Runaway: Exact Moment Bounds from an Operator Conservation Law*
> Christopher Ewasiuk, Stefano Profumo — [arXiv:2604.21348](https://arxiv.org/abs/2604.21348)

---

## Overview

Ghost degrees of freedom — fields with a wrong-sign kinetic term — are typically dismissed as catastrophically unstable: energy is unbounded below, so coupling a ghost to a normal sector should trigger runaway pair production. This work shows that instability is not kinematically inevitable. Given a potential that classically confines the ghost, the quantum system obeys an **exact operator conservation law** that places a rigorous, state-independent upper bound on the mean-squared phase-space radius for all time.

This repository contains the full numerical framework used to derive and verify that result across three independent approaches.

---

## Key Results

- **Exact conservation law:** A classical conserved quantity lifts to a quantum operator that commutes exactly with the full ghost Hamiltonian — with no ℏ corrections. This is not an approximation.
- **Rigorous moment bound:** The mean-squared phase-space radius ⟨r²⟩ satisfies a provable upper bound for all time, derived analytically from the conserved operator.
- **Three independent numerical confirmations:**
  - Heisenberg picture — direct operator evolution of moments
  - Schrödinger picture — full wavefunction time evolution
  - Fock-space diagonalization — eigenspectrum and overlap analysis
- All three frameworks confirm wavepacket confinement below the analytic bound.

---

## Repository Structure

```
Bound-Ghosts/
├── bound_ghosts.ipynb              # Classical analysis: trajectories, potential, stability map
├── bound_ghosts_quantum.ipynb      # Quantum analysis: all three numerical frameworks
├── ghost_states/                   # Rendered Fock-space eigenstate probability densities
├── PT_norm.png                     # PT-norm structure
├── classical_trajectories.png      # Phase-space trajectories confirming classical boundedness
├── potential.png                   # Ghost potential landscape
├── stability_map.png               # Parameter-space stability scan
├── spectrum_analysis.png           # Energy spectrum of the ghost Hamiltonian
├── spectrum_analysis_24_states.png # Spectrum for first 24 states
├── spectrum_ordered_fock_highN.png # High-N Fock-ordered spectrum
├── level_repulsion.png             # Level repulsion structure
├── initial_state.png               # Initial wavepacket configuration
├── wavepacket_snapshots.png        # Time evolution of wavepacket
├── wavefunction_snapshots.png      # Wavefunction cross-sections over time
├── heisenberg_moments.png          # Moment evolution in Heisenberg picture
├── lambda_scan.png                 # Coupling constant scan
└── schrodinger_diagnostics.png     # Schrödinger evolution diagnostics
```

---

## Notebooks

### `bound_ghosts.ipynb` — Classical Analysis
- Constructs the ghost potential and verifies classical boundedness
- Computes and visualizes phase-space trajectories
- Generates the stability map across the parameter space
- Derives the classical conserved quantity that motivates the quantum result

### `bound_ghosts_quantum.ipynb` — Quantum Analysis
- **Fock-space diagonalization:** builds the Hamiltonian matrix in the harmonic oscillator basis, diagonalizes it, computes the full eigenspectrum and eigenstate wavefunctions
- **Heisenberg picture:** evolves quantum moments directly as operators, tracks ⟨x²⟩, ⟨p²⟩, and ⟨r²⟩ against the analytic bound
- **Schrödinger picture:** full wavefunction time evolution via split-operator or matrix exponentiation, confirms spatial confinement
- Generates all figures used in the paper

---

## Dependencies

```bash
pip install numpy scipy matplotlib jupyter
```

All computations run in standard Python scientific stack. No GPU required.

---

## Citation

```bibtex
@article{Ewasiuk:2026ghost,
  author  = {Ewasiuk, Christopher and Profumo, Stefano},
  title   = {Ghost Degrees of Freedom Without Quantum Runaway:
             Exact Moment Bounds from an Operator Conservation Law},
  year    = {2026},
  eprint  = {2604.21348},
  archivePrefix = {arXiv},
  primaryClass  = {quant-ph}
}
```

---

## Author

**Christopher Ewasiuk** — PhD candidate, UC Santa Cruz
[chrisewasiuk.com](https://chrisewasiuk.com) · [cewasiuk@ucsc.edu](mailto:cewasiuk@ucsc.edu)
