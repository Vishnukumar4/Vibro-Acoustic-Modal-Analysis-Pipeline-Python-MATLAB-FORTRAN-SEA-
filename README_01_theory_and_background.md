# README 01 — Vibro-Acoustic Theory and Background

## What Is Vibro-Acoustic Simulation?

Vibro-acoustic simulation studies the interaction between structural vibration and sound radiation. When a structure vibrates, it can transfer energy into the surrounding acoustic field. Similarly, acoustic pressure can excite structural vibration.

This type of simulation is important in:

- Vehicle noise and vibration analysis
- Aerospace cabin noise reduction
- Building acoustics
- Machine enclosure design
- Acoustic absorber design
- Transmission loss prediction
- Structural dynamics education

---

## Frequency Ranges in Vibro-Acoustics

Different numerical methods are useful in different frequency ranges.

| Frequency Range | Typical Method | Reason |
|---|---|---|
| Low frequency | FEM / deterministic methods | Individual modes can be resolved clearly |
| Mid frequency | Hybrid FEM/SEA | Some parts are modal, some are diffuse/random |
| High frequency | SEA / statistical methods | Too many modes for full deterministic simulation |

The mid-frequency range is difficult because neither pure FEM nor pure SEA is always sufficient. This is why hybrid FEM/SEA methods are useful.

---

## FEM Concept

The Finite Element Method divides a structure or acoustic domain into smaller elements. The physical response is solved using matrix equations.

A typical structural dynamic equation is:

```text
M q_ddot + C q_dot + K q = F
```

In the frequency domain, this becomes:

```text
D(w) q(w) = F(w)
```

where:

| Symbol | Meaning |
|---|---|
| `M` | Mass matrix |
| `C` | Damping matrix |
| `K` | Stiffness matrix |
| `D(w)` | Dynamic stiffness matrix |
| `q(w)` | Frequency-domain displacement response |
| `F(w)` | Applied force vector |

The dynamic stiffness form is useful because it allows simulation over a frequency sweep.

---

## BEA / BEM Concept

Boundary Element Analysis is commonly used for acoustic radiation and scattering problems. Instead of meshing the entire acoustic volume, BEA/BEM focuses on the boundary surface.

In this student project, BEA concepts were used at a methodology level for understanding:

- Acoustic radiation from vibrating surfaces
- Pressure response near radiating panels
- Boundary-based acoustic coupling
- Frequency response interpretation

---

## SEA Concept

Statistical Energy Analysis models the average flow of vibrational or acoustic energy between subsystems.

Instead of solving every mode directly, SEA describes the system using:

- Modal density
- Damping loss factors
- Coupling loss factors
- Input power
- Subsystem energy

A simplified SEA balance equation is:

```text
SEA Matrix * Energy Vector = Input Power Vector
```

SEA is useful when the system has many modes and the exact deterministic response is less important than the average energy behavior.

---

## Hybrid FEM/SEA Concept

Hybrid FEM/SEA combines deterministic and statistical modeling.

A typical hybrid case is:

```text
Diffuse acoustic room  <-->  deterministic FE plate  <-->  diffuse acoustic room
```

The FE plate is modeled deterministically because its modes are important, while the rooms are modeled statistically because their acoustic fields may be diffuse.

This approach is especially useful in the mid-frequency range.

---

## Transfer Matrix Method

The transfer matrix method is useful for layered acoustic structures such as:

- Porous absorbers
- Perforated panels
- Air gaps
- Double walls
- Poroelastic layers
- Noise control treatment stacks

A layered system can be represented as a sequence of matrices that transfer pressure, velocity, stress, or displacement states from one layer interface to another.

Example layered structure:

```text
Air -> Perforated Plate -> Porous Absorber -> Rigid Backing
```

This project uses transfer-matrix-style thinking to estimate absorption coefficient, impedance, and transmission loss.

---

## Main Engineering Outputs

| Output | Meaning |
|---|---|
| Modal density | Number of modes per frequency interval |
| Modal overlap | How strongly modes overlap in frequency |
| Radiation efficiency | How efficiently a structure radiates sound |
| Absorption coefficient | Fraction of acoustic energy absorbed |
| Transmission loss | Sound insulation performance in dB |
| Pressure response | Acoustic pressure level across frequency |
| Velocity response | Structural vibration response across frequency |
| Coupling loss factor | Energy transfer between SEA subsystems |

---

## Student Understanding

The main learning goal was to understand how vibro-acoustic simulation combines structural dynamics, acoustics, numerical methods, and frequency-domain post-processing. Instead of treating FEM, BEA, SEA, and transfer matrix models as separate topics, this project connects them into one simulation pipeline.
