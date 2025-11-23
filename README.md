# Monte Carlo Simulation of Polymer Folding

The results can be found in **FINAL_DRAFT_PROJECT1.ipynb**.

This project focuses on simulating polymer folding and dynamics using Monte Carlo methods. The goal is to study how polymers change their conformation under different temperatures and interaction potentials, and to estimate their energy and diameter in various states.

## Project Overview

Polymers are long chains of repeating units (monomers), and their conformation determines their physical and chemical properties. In this project, we implemented both deterministic and stochastic methods to model polymer behavior:

### Numerical Representation

- **Absolute coordinates `(N,2)`** for efficient energy and diameter calculations.
- **Relative coordinates `(N-1)`** for fast rotation operations.
- A **hybrid approach** combines the strengths of both representations.

### Rotation and Validation

- Monte Carlo rotations with self-avoidance checks.
- Performance optimization using **Numba JIT** to accelerate computationally intensive functions.

### Energy Calculations

- Symmetric potential matrices model attractive/repulsive interactions between monomers.
- Energies computed using `scipy.spatial.distance.cdist`.

### Monte Carlo Simulations

- **Metropolis algorithm** for sampling thermodynamic equilibrium.
- Temperature-dependent folding and energy distribution.
- Estimation of polymer diameter, including simulations of crystallization processes.

### Visualization

- 2D plotting of polymer configurations with color-coded monomers.
- Graphical representation of energy and diameter over Monte Carlo steps.

## Key Results

- Polymer energy and diameter increase with temperature.
- At low temperatures, polymers are often trapped in local energy minima.
- Gradual cooling induces crystallization, forming low-energy compact structures.
- Hybrid `(N-1) + (N,2)` representation significantly reduces runtime for rotations.
- Computation time scales linearly with polymer length, enabling simulations of larger systems.

## Technical Skills Demonstrated

- **Programming & Optimization:** Python, Numpy, Scipy, Numba JIT, matplotlib.
- **Numerical Simulation:** Monte Carlo methods, Metropolis algorithm, stochastic processes.
- **Data Analysis:** Energy computation, standard deviation, temperature-dependent behavior.
- **Scientific Visualization:** 2D polymer plots, energy and diameter evolution over time.
- **Scientific Modeling:** Polymer physics, interaction potentials, crystallization processes.

## Applications

This project demonstrates skills relevant to:

- **Material Science:** Designing and analyzing new polymer materials.
- **Biophysics:** Modeling protein and nucleic acid folding.
- **Computational Physics:** Understanding thermodynamics and kinetics in molecular systems.
