# README 05 — Student Project Experience

## Project Title

**Vibro-Acoustic Modal Analysis Pipeline**  
**Python | MATLAB | FORTRAN | FEM/BEA Concepts | SEA Concepts | Hybrid FEM/SEA**

---

## Student Project Description

This project was developed as a student simulation project to understand vibro-acoustic behavior in coupled structural-acoustic systems. The goal was to build a clear workflow for modeling vibration, acoustic pressure response, transmission loss, absorption, and energy flow using open simulation tools and documented numerical methods.

The project focused on learning how deterministic methods such as FEM and transfer matrix models can be combined with statistical approaches such as SEA. I also studied how hybrid FEM/SEA methods are used when a system contains both low-frequency deterministic behavior and high-frequency diffuse energy behavior.

---

## What I Built

I built a structured simulation pipeline that included:

- Python scripts for vibro-acoustic model setup and automation
- MATLAB-style plotting workflows for post-processing and verification
- FORTRAN-style numerical solver organization for frequency-domain matrix solving
- Documentation for FEM, BEA, SEA, transfer matrix, and hybrid FEM/SEA concepts
- Case studies for absorbers, double walls, room-panel-room systems, and box enclosures
- Professional GitHub README files for explaining methodology and results

---

## Technical Work Performed

### Modal Analysis

I studied modal behavior of structural plates and acoustic systems by analyzing:

- Modal density
- Modes in frequency bands
- Modal overlap
- Natural frequency behavior
- Plate velocity response

This helped me understand when a deterministic modal model is useful and when statistical modeling becomes more practical.

---

### Frequency Response Simulation

I created a frequency-domain workflow where the response is calculated over a sweep of frequencies.

Engineering outputs included:

- Structural velocity response
- Acoustic pressure response
- Transmission loss
- Absorption coefficient
- Radiation efficiency

---

### SEA-Based Modeling

I applied Statistical Energy Analysis concepts to model systems with multiple coupled subsystems.

Examples:

- Room 1 to wall to room 2
- Acoustic cavity to vibrating panels
- Plate-to-room coupling
- Double-wall cavity energy transfer

This helped me understand energy balance, coupling loss factors, and subsystem energy response.

---

### Hybrid FEM/SEA Modeling

I studied hybrid modeling where a deterministic FE plate is coupled between statistical acoustic rooms.

This helped me understand the mid-frequency challenge in vibro-acoustics, where pure FEM can become expensive and pure SEA may not capture deterministic modal behavior accurately.

---

### Data Processing and Documentation

I organized the simulation results into readable tables and plots.

I documented:

- Assumptions
- Material properties
- Frequency ranges
- Simulation cases
- Result interpretation
- Lessons learned

This made the project easier to present in GitHub, reports, and interviews.

---

## Challenges Faced

### 1. Understanding Different Simulation Methods

Vibro-acoustic simulation requires many methods. I had to understand the role of FEM, BEA, SEA, transfer matrix methods, and hybrid methods instead of treating them as isolated topics.

### 2. Frequency Range Selection

The correct method depends strongly on the frequency range. I learned how low-frequency, mid-frequency, and high-frequency models require different assumptions.

### 3. Coupled System Interpretation

It was challenging to understand how vibration in a structure becomes acoustic pressure in a room and how acoustic energy transfers back into a structure.

### 4. Result Interpretation

I learned that simulation plots must be explained physically. For example, a transmission loss curve should be connected to mass law, cavity resonance, damping, and absorber behavior.

### 5. Documentation Quality

A technical project is stronger when it is documented clearly. I separated the project into multiple README files so that the theory, implementation, simulation cases, results, and student learning experience are easy to follow.

---

## Skills Demonstrated

| Skill | Demonstrated Through |
|---|---|
| Python simulation | Model setup, automation, plotting |
| MATLAB post-processing | Frequency response plotting and result checking |
| FORTRAN solver concepts | Matrix solver and frequency sweep methodology |
| FEM concepts | Modal response and dynamic stiffness understanding |
| BEA concepts | Acoustic radiation and boundary response understanding |
| SEA concepts | Energy balance and subsystem coupling |
| Hybrid FEM/SEA | FE plate coupled with statistical acoustic rooms |
| Data analysis | Transmission loss, absorption, pressure, velocity plots |
| Documentation | Multi-file GitHub README structure |

---

## Resume Bullet Version

**Vibro-Acoustic Modal Analysis Pipeline — Python, MATLAB, FORTRAN, SEA Concepts**

- Developed a vibro-acoustic simulation pipeline using Python and MATLAB to analyze modal response, structural vibration, acoustic pressure, and sound transmission across coupled systems.
- Applied FEM, BEA, transfer matrix, and SEA concepts for frequency-response analysis, absorber modeling, double-wall transmission loss, and room-panel-room acoustic simulations.
- Used FORTRAN-style numerical solver methodology for dynamic stiffness matrix solving, frequency sweeps, and modal response computation.
- Automated vibro-acoustic data processing, plotted transmission loss and absorption results, and documented structural dynamics methodology in a professional GitHub-ready format.

---

## Interview Explanation

This was a simulation-focused student project where I built a vibro-acoustic analysis pipeline to study how structural vibration and acoustic fields interact. I used Python for simulation scripting and MATLAB-style workflows for post-processing. The project covered FEM concepts for deterministic modal response, SEA concepts for high-frequency energy flow, and hybrid FEM/SEA methodology for mid-frequency coupled systems.

One important part of the project was learning how to model a room-panel-room system, where acoustic energy from one room excites a structural wall and transfers sound into another room. I also studied layered absorber and double-wall configurations to evaluate absorption coefficient and transmission loss. The project helped me understand structural dynamics, acoustic coupling, frequency-domain simulation, and professional documentation of engineering results.

---

## Final Learning Summary

This project helped me connect theory with implementation. I learned how vibro-acoustic systems are modeled using matrices, energy equations, material properties, and frequency-domain simulation. I also learned how to explain simulation results clearly, which is important for both engineering reports and technical interviews.
