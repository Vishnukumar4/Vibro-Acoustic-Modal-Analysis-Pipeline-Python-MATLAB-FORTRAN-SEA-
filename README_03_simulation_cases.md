# README 03 — Simulation Case Studies

This project is organized around multiple vibro-acoustic simulation cases. Each case represents a common engineering problem in structural acoustics.

---

## Case 1 — Porous Absorber Simulation

### Objective

Estimate the absorption coefficient of porous absorber layers over a frequency range.

### System

```text
Incident acoustic wave -> porous/fibrous layer -> backing condition
```

### Inputs

| Parameter | Example |
|---|---|
| Porosity | 0.98 |
| Flow resistivity | 25000 Ns/m^4 |
| Tortuosity | 1.02 |
| Layer thickness | 0.10 m or 0.20 m |
| Frequency range | 10 Hz to 10 kHz |

### Outputs

- Diffuse-field absorption coefficient
- Normal-incidence absorption coefficient
- Surface impedance

### Student Work

I created a frequency sweep, defined porous material parameters, computed absorption response, and plotted the absorber performance. This helped me understand how material thickness and flow resistivity influence low-frequency and mid-frequency absorption.

---

## Case 2 — Double Wall Transmission Loss

### Objective

Simulate transmission loss through layered double-wall systems.

### System

```text
Air -> aluminum panel -> air/foam cavity -> limp mass or second panel -> air
```

### Inputs

| Parameter | Example |
|---|---|
| First panel | 1 mm aluminum |
| Cavity | 5 cm air or fibre layer |
| Added mass | 1 kg/m^2 or 2.7 kg/m^2 |
| Frequency range | 30 Hz to 10 kHz |

### Outputs

- Transmission coefficient
- Transmission loss in dB
- Effect of cavity material
- Effect of second mass layer

### Transmission Loss Formula

```text
TL = -10 log10(tau)
```

where `tau` is the acoustic transmission coefficient.

### Student Work

I compared different double-wall configurations and observed how cavity filling and mass layers improve sound insulation. The result was documented using transmission loss plots across frequency.

---

## Case 3 — Material Parameter Identification

### Objective

Estimate porous material parameters by fitting simulation response to impedance data.

### Parameters Estimated

- Tortuosity
- Viscous characteristic length
- Thermal characteristic length

### Workflow

```text
1. Load measured impedance data
2. Define porous material model
3. Run impedance simulation
4. Compare simulated and measured impedance
5. Minimize error using optimization
```

### Cost Function

```text
Cost = sum(|Z_simulated - Z_measured|^2)
```

### Student Work

I used optimization concepts to fit porous material parameters and compare simulated impedance with reference impedance data. This connected acoustic modeling with data-driven parameter identification.

---

## Case 4 — Room-Panel-Room SEA Model

### Objective

Model sound transmission between two rooms separated by a structural wall.

### System

```text
Room 1 -> Wall -> Room 2
```

### SEA Subsystems

| Subsystem | Type |
|---|---|
| Room 1 | Acoustic SEA system |
| Wall | Structural plate system |
| Room 2 | Acoustic SEA system |

### Outputs

- Modal density
- Modal overlap
- Radiation efficiency
- Coupling loss factors
- Room pressure response
- Wall velocity response
- Transmission loss

### Student Work

I created a coupled room-wall-room model and evaluated energy transfer from the source room to the receiving room. This helped me understand how SEA represents average energy flow between acoustic and structural subsystems.

---

## Case 5 — Box Cover Noise Radiation

### Objective

Simulate a sound source inside a box enclosure and estimate acoustic radiation through the surrounding panels.

### System

```text
Internal acoustic cavity -> vibrating steel panels -> exterior radiation
```

### Model Components

- Five steel plate subsystems
- Internal acoustic cavity
- Area junctions between room and panels
- Line junctions between connected panels
- Semi-infinite fluid radiation paths

### Outputs

- Internal pressure response
- Panel velocity response
- Radiated power
- Insertion loss

### Student Work

I modeled an enclosure around a sound source and compared untreated and treated configurations. This case helped me understand how noise control treatments reduce radiated sound power.

---

## Case 6 — Box Cover with Noise Control Treatment

### Objective

Evaluate how porous layers and added mass improve acoustic isolation.

### Treatment Configuration

```text
Steel panel -> fibre layer -> limp mass layer
```

### Outputs

- Absorption area
- Treated panel response
- Radiated power reduction
- Insertion loss improvement

### Student Work

I compared the untreated box model with a noise-control-treated model. This showed how acoustic treatments influence both internal absorption and structural radiation.

---

## Case 7 — Hybrid FEM/SEA Plate Model

### Objective

Use a deterministic finite-element plate between two statistical acoustic rooms.

### System

```text
SEA Room 1 -> FE Plate -> SEA Room 2
```

### Hybrid Features

- FE plate mode shapes
- Modal response calculation
- Acoustic SEA subsystems
- Hybrid area junction
- Energy-to-response conversion

### Outputs

- FE plate velocity response
- Room pressure response
- Transmission loss
- Coupling factors

### Student Work

I studied how a deterministic FE plate can be embedded into a larger SEA model. This was the most important mid-frequency simulation case because it combined deterministic and statistical modeling.

---

## Summary Table

| Case | Method | Main Output |
|---|---|---|
| Porous absorber | Transfer matrix | Absorption coefficient |
| Double wall | Transfer matrix / SEA concepts | Transmission loss |
| Material fitting | Optimization | Porous material parameters |
| Room-panel-room | SEA | Energy, pressure, velocity, TL |
| Box enclosure | SEA | Radiated power, insertion loss |
| Treated box | SEA + transfer matrix | Noise reduction |
| Hybrid plate | FEM/SEA | Mid-frequency coupled response |
