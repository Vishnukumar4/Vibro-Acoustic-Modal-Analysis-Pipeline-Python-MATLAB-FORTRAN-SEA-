# README 02 — Simulation Pipeline and Implementation

## Project Pipeline

The project was organized as a complete vibro-acoustic simulation workflow.

```text
1. Define geometry and materials
2. Define frequency range
3. Build structural or acoustic model
4. Apply loads or acoustic excitation
5. Solve system response
6. Extract physical quantities
7. Post-process using Python / MATLAB
8. Document results and observations
```

---

## Software Stack

| Tool | Role in Project |
|---|---|
| Python | Main simulation scripting and automation |
| MATLAB | Verification plots and post-processing style workflow |
| FORTRAN | Numerical solver methodology and matrix-based solver concepts |
| NumPy | Array and matrix operations |
| SciPy | Optimization and numerical utilities |
| Matplotlib | Plot generation |
| Markdown | Documentation and GitHub README writing |

---

## Suggested Repository Structure

```text
Vibro-Acoustic-Modal-Analysis-Pipeline/
|
├── README.md
├── README_01_theory_and_background.md
├── README_02_pipeline_and_implementation.md
├── README_03_simulation_cases.md
├── README_04_results_and_postprocessing.md
├── README_05_student_experience.md
|
├── src/
|   ├── python/
|   |   ├── absorber_simulation.py
|   |   ├── double_wall_transmission.py
|   |   ├── room_panel_room_sea.py
|   |   ├── hybrid_fem_sea_plate.py
|   |   └── postprocess_results.py
|   |
|   ├── matlab/
|   |   ├── plot_frequency_response.m
|   |   ├── plot_transmission_loss.m
|   |   └── compare_results.m
|   |
|   └── fortran/
|       ├── dynamic_matrix_solver.f90
|       ├── frequency_sweep_solver.f90
|       └── modal_response_solver.f90
|
├── data/
|   ├── material_properties.csv
|   ├── frequency_axis.csv
|   └── impedance_measurements.csv
|
├── results/
|   ├── absorption_results.csv
|   ├── transmission_loss_results.csv
|   ├── modal_density_results.csv
|   └── pressure_velocity_results.csv
|
├── figures/
|   ├── absorber_absorption.png
|   ├── double_wall_TL.png
|   ├── room_pressure_response.png
|   └── modal_density.png
|
└── docs/
    ├── methodology_notes.md
    ├── assumptions.md
    └── final_report.md
```

---

## Implementation Flow

### 1. Geometry Definition

The first step is defining the system geometry.

Example systems:

- Rectangular plate
- Acoustic room
- Double wall cavity
- Box enclosure
- Layered absorber
- Perforated panel with porous backing

Example parameters:

```text
Plate length       = 0.8 m
Plate width        = 0.5 m
Plate thickness    = 4 mm
Room volume        = 64 m^3
Frequency range    = 25 Hz to 4000 Hz
```

---

### 2. Material Definition

Material properties are defined for structural and acoustic subsystems.

Example structural properties:

```text
Young's modulus
Density
Poisson's ratio
Damping loss factor
Thickness
```

Example acoustic material properties:

```text
Air density
Speed of sound
Flow resistivity
Porosity
Tortuosity
Viscous characteristic length
Thermal characteristic length
```

---

### 3. Frequency Axis Setup

The simulation runs over a frequency sweep.

Examples:

```python
freq = np.geomspace(25, 4000, 150)
omega = 2 * np.pi * freq
```

For SEA models, octave-band or one-third-octave-band frequency axes are useful.

---

### 4. Matrix Assembly

The dynamic stiffness matrix is assembled for deterministic response.

```text
D(w) = K - w^2 M + j w C
```

The SEA matrix is assembled for energy balance.

```text
SEA_matrix(w) * subsystem_energy(w) = input_power(w)
```

---

### 5. Solver Execution

The solver loops over frequency points.

Pseudo-code:

```text
for each frequency:
    assemble dynamic matrix
    apply load vector
    solve response
    store displacement, velocity, pressure, or energy
```

FORTRAN-style numerical solver modules were included conceptually for:

- Efficient matrix solving
- Frequency sweep loops
- Modal response calculation
- Structured numerical workflow

---

### 6. Post-Processing

The final response is converted into engineering outputs.

Examples:

```text
Velocity RMS
Pressure RMS
Absorption coefficient
Transmission loss
Modal density
Radiation efficiency
Coupling loss factors
```

---

## Example Python Workflow

```python
import numpy as np
import matplotlib.pyplot as plt

freq = np.geomspace(100, 10000, 200)
omega = 2 * np.pi * freq

# Placeholder example response
transmission_coefficient = 1 / (1 + (freq / 1000)**2)
transmission_loss = -10 * np.log10(transmission_coefficient)

plt.semilogx(freq, transmission_loss)
plt.xlabel("Frequency [Hz]")
plt.ylabel("Transmission Loss [dB]")
plt.grid(True, which="both")
plt.show()
```

---

## MATLAB Post-Processing Example

```matlab
freq = readmatrix('results/frequency_axis.csv');
TL = readmatrix('results/transmission_loss_results.csv');

semilogx(freq, TL, 'LineWidth', 1.5);
grid on;
xlabel('Frequency [Hz]');
ylabel('Transmission Loss [dB]');
title('Double Wall Transmission Loss');
```

---

## FORTRAN Solver Concept

```fortran
program frequency_sweep_solver
    implicit none

    ! Define frequency loop
    ! Assemble dynamic stiffness matrix
    ! Solve D(w) q(w) = F(w)
    ! Store response for post-processing

end program frequency_sweep_solver
```

FORTRAN was used in the project description as a numerical-solver component because many engineering simulation codes rely on efficient compiled solvers for matrix operations and frequency sweeps.

---

## Student Implementation Notes

The project was structured to look like a realistic simulation workflow. Each script had a specific purpose: define physics, solve response, generate result files, and create plots. This made the repository easier to present in GitHub and easier to explain during interviews.
