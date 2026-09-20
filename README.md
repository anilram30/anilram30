# Hi, I'm Sreeram Anil

Master's-thesis control engineer at **FAU Erlangen-Nürnberg**, based in Bavaria. Writing my thesis on SLQP-MPC for a Quanser RT2 linear inverted pendulum.
Looking for a **Werkstudent** position in control, estimation, signal processing, robotics or embedded systems.

📍 Nürnberg, Germany  ·  📧 [sreeramanil30@gmail.com](mailto:sreeramanil30@gmail.com)


---

## estkit

A header-only C++17 library and benchmark of multi purpose **86 state estimators and observers**. Implemented for battery-management systems in electric aircraft, with aerospace attitude-estimation heritage. Every algorithm is an original implementation from its primary publication, embedded-safe by construction (no heap, no exceptions, float32-ready, Cortex-M7 verified in CI), and cross-validated against FilterPy, PyBaMM and ahrs.

**Repo:** [estkit](https://github.com/anilram30/estkit)  ·  **Site:** [anilram30.github.io/estkit](https://anilram30.github.io/estkit/)  ·  **Report:** 958 pages, one chapter per estimator

`86 estimators · 12 families · 2 truth plants · 12 fault scenarios · ~9,000 benchmark runs · 0 runtime dependencies`

Code Apache 2.0, report and data CC BY 4.0.

---

## HF cable toolchain

Seven engineering packages that take a high-frequency cable from raw network-analyser measurement to a predicted automotive-Ethernet link. Each package has its own test suite, command-line interface, technical report and CI.

**Site:** [anilram30.github.io/hf-cable](https://anilram30.github.io/hf-cable/)  ·  **Hub:** [hf-cable-toolchain](https://github.com/anilram30/hf-cable-toolchain)

| | Package | What it does |
|---|---|---|
| **A** | [cablecheck](https://github.com/anilram30/cablecheck) | Measurement → standards-based verdict and report |
| **B** | [labauto](https://github.com/anilram30/labauto) | Calibration gates, validation, sealed traceable archive |
| **C** | [shieldeval](https://github.com/anilram30/shieldeval) | Legacy-style shielding tool reconstruction, then modernised |
| **D** | [zprofile](https://github.com/anilram30/zprofile) | Impedance against position from a scattering measurement |
| **E** | [cableanalytics](https://github.com/anilram30/cableanalytics) | Production records → predicted electrical performance |
| **F** | [labplatform](https://github.com/anilram30/labplatform) | Multi-site metrology, uncertainty budgets, drift detection |
| **G** | [linktwin](https://github.com/anilram30/linktwin) | Full-link digital twin — pass/fail, eye at receiver, probability of passing |

---

## Control and estimation — in progress

- **Distributed MPC + MHE drone clustering** — cooperative control across a heterogeneous UAV cluster.
- **ANYmal walking-simulation framework** — joint NMPC + NMHE for quadrupedal locomotion.
- **Real-time-iteration NMPC and NMHE solvers** — ultra-fast solvers with state and input constraints, targeted at embedded control.
* **AEROFORGE — Autonomous aerial construction** — heterogeneous UAVs cooperatively assemble and verify a bridge using distributed estimation and real-time NMPC under cable, contact, wind, and actuator constraints.

_Repositories will be published as each project reaches a shareable state._

---

## Tech

**Languages** C++17 · MATLAB · Python · C · some C# and Java
**Control and estimation** MPC, MHE, Kalman and sigma-point filters, particle filters, moving-horizon estimation, quadratic programming, Monte Carlo, sensitivity analysis
**Hardware** STM32 (Cortex-M7, STM32Cube, HAL), Quanser real-time systems
**Tooling** git, CMake, pytest, ruff, GitHub Actions CI, pandoc + XeLaTeX for reports

---

## Contact

**Email** [sreeramanil30@gmail.com](mailto:sreeramanil30@gmail.com)
**Location** Nürnberg, Bavaria — open to relocation across Bavaria for the right role.

---

_The engineering decisions, algorithm and system design, validation strategy, analysis and stated limitations are my own._
