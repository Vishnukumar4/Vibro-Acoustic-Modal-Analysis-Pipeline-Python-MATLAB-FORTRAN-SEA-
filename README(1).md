# Vibro-Acoustic Modal Analysis Pipeline

**Python | MATLAB | FORTRAN | FEM/BEA Concepts | SEA Concepts | Hybrid FEM/SEA Simulation**

This repository presents a student-style vibro-acoustic simulation project focused on modal analysis, structural vibration response, acoustic transmission, and Statistical Energy Analysis (SEA)-based system modeling.

The project was designed to make vibro-acoustic simulation easier to understand for students by combining open-source Python workflows, MATLAB post-processing, numerical solver concepts, and structured documentation. The workflow is inspired by the type of simulation environment provided by the `pyva` toolbox, which supports deterministic models, random SEA systems, hybrid FEM/SEA models, transfer matrix models, material modeling, loads, geometry handling, and matrix/vector data structures.

---

## Project Summary

Vibro-acoustic simulation studies how vibrating structures generate and transmit sound. This project focuses on the simulation workflow used for structures such as panels, rooms, layered absorbers, double walls, and acoustic cavities.

The main project objective was to build a clear simulation pipeline that can be understood and extended by students working in acoustics, structural dynamics, or mechanical/computer engineering.

The pipeline covers:

- Structural modal analysis
- Frequency response simulation
- Sound transmission and transmission loss estimation
- Absorber and layered material modeling
- SEA-based room-panel-room simulation
- Hybrid FEM/SEA concepts for mid-frequency vibro-acoustics
- Data processing and visualization using Python and MATLAB
- Numerical solver documentation with FORTRAN-style matrix workflow

---

## Resume-Style Project Description

**Vibro-Acoustic Modal Analysis Pipeline — Python, MATLAB, FORTRAN, SEA Concepts**

- Developed a vibro-acoustic simulation pipeline using Python and MATLAB to study structural vibration, acoustic response, modal behavior, and sound transmission across coupled systems.
- Applied FEM, BEA, transfer matrix, and SEA concepts to simulate frequency response, modal density, radiation efficiency, transmission loss, and coupled room-panel-room behavior.
- Used FORTRAN-style numerical solver methodology for matrix-based dynamic stiffness systems, frequency-domain response solving, and post-processing of acoustic/structural simulation results.
- Automated vibro-acoustic data processing, frequency sweep analysis, plotting, and professional documentation of structural dynamics methodology and findings.

---

## Why This Project Matters

Commercial vibro-acoustic simulation tools can be expensive and difficult for students to access. This project demonstrates how a student can learn the core simulation workflow using open tools and documented numerical methods.

The focus is not only on running simulations, but also on understanding:

- What physical system is being modeled
- Which frequency range is being analyzed
- When deterministic methods such as FEM are useful
- When statistical methods such as SEA are more appropriate
- How hybrid FEM/SEA methods connect deterministic and random systems
- How acoustic materials and layered structures affect sound absorption and transmission

---

## Repository Documentation

This repository is split into multiple README files so the project is easier to understand:

| File | Purpose |
|---|---|
| `README.md` | Main project overview |
| `README_01_theory_and_background.md` | Vibro-acoustic theory, FEM, BEA, SEA, and hybrid FEM/SEA concepts |
| `README_02_pipeline_and_implementation.md` | Simulation pipeline, tools, folder structure, and implementation flow |
| `README_03_simulation_cases.md` | Student simulation case studies such as absorber, double wall, rooms, and box cover |
| `README_04_results_and_postprocessing.md` | Result metrics, plots, tables, and MATLAB/Python post-processing |
| `README_05_student_experience.md` | Student learning experience, challenges, and resume bullets |

---

## Example Applications

The project can be used to simulate or document:

- Single panel modal response
- Room-panel-room acoustic transmission
- Double-wall transmission loss
- Porous absorber absorption coefficient
- Poroelastic material response
- Box cover noise radiation
- SEA energy flow between acoustic and structural subsystems
- Hybrid FEM/SEA coupling between deterministic plates and diffuse acoustic fields

---

## Tools and Concepts

| Category | Tools / Concepts |
|---|---|
| Programming | Python, MATLAB, FORTRAN-style numerical solvers |
| Simulation Methods | FEM, BEA concepts, SEA, hybrid FEM/SEA, transfer matrix method |
| Physics | Structural dynamics, acoustic radiation, modal density, transmission loss |
| Data Processing | NumPy, SciPy, Matplotlib, MATLAB plotting |
| Documentation | Markdown README files, simulation notes, result tables |

---

## Student Learning Outcome

By completing this project, I gained experience in building a complete simulation workflow instead of only running a single script. I learned how vibro-acoustic systems are modeled, how structural and acoustic domains are coupled, how SEA describes high-frequency energy flow, and how frequency-domain results can be processed into engineering metrics such as transmission loss, absorption coefficient, pressure response, and velocity response.
