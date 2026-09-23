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

## Apollo circumlunar navigation

 **Site:** [anilram30.github.io/Apollo-Trajectory-Recreation](https://anilram30.github.io/Apollo-Trajectory-Recreation/) 
 
The **first Kalman filter to fly** — NASA TR R-135 (Smith, Schmidt & McGee, 1962) — reconstructed in MATLAB from the original documents and flown over a complete Earth → Moon → Earth ballistic free-return mission. A genuine figure-8 trajectory targeted in the full Earth(J2) + Moon + Sun field, optical-angle sightings with the horizon-altitude bias measured on Apollo 13's own P23 data, and both variants of the filter: the nominal-linearized form as first published, and the estimate-linearized form R-135 already recommended and history later named the EKF.

**Repo:** [Apollo-Trajectory-Recreation](https://github.com/anilram30/Apollo-Trajectory-Recreation)  ·  **Report:** 13-page narrative through the primary NASA sources . 

`5.72-day free-return mission · 10-state augmented filter · 1,986 sextant sightings · 31,000 km open-loop miss → 1.4 km EKF error · 2 MATLAB files`

Code Apache 2.0, report and data CC BY 4.0.

---

## UAV cluster — distributed MPC and MHE

Distributed model-predictive control and moving-horizon estimation for a heterogeneous UAV cluster — quaternion hexacopters and 6-DOF fixed-wing aircraft, each agent running its own constrained real-time estimator and controller, coordinating over a communication graph with no central node. Six hexacopters hold formation through a ten-second GNSS blackout: the distributed estimator fuses relative measurements to GNSS-good neighbours and pins each denied agent to within nine centimetres of truth while dead reckoning drifts past a metre. The **anchor-coverage** condition on the communication graph is identified as the structural limit, and a leveled multi-hop anchoring extension recovers the broken case with the safety margin restored. The report derives both airframes from first principles; the compiled real-time solvers substituted into the closed loop reproduce the reference behaviour without change.

**Repo:** [uav-cluster-dmpc-dmhe](https://github.com/anilram30/uav-cluster-dmpc-dmhe)  ·  **Site:** [anilram30.github.io/uav-cluster-dmpc-dmhe](https://anilram30.github.io/uav-cluster-dmpc-dmhe/)  ·  **3D replay:** [SwarmScope](https://anilram30.github.io/uav-cluster-dmpc-dmhe/swarmscope.html)  ·  **Report:** 57 pages, first-principles derivations of both airframes

`6 hexacopters + 4 fixed-wing aircraft · 13-state quaternion plants · 210-run Monte-Carlo campaign, 0 divergences · dead-reckoning 1.26 m → DMHE 0.088 m · min separation 1.55 m against 1.4 m barrier · compiled solvers in-loop ≈76 µs / agent / cycle`

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


---

ANYmal-C — Unified framework walking control by NMPC + moving-horizon estimation

(Repo private for now, working on a clonable ACADOS version backend that can run simulations as an alternative)

A unified single-rigid-body framework where a nonlinear model-predictive controller and a nonlinear moving-horizon estimator share one reduced-order model, one symbolic source, and one design language, closing an output-feedback trot on a full-body ANYmal-C simulation in MuJoCo. The estimator reconstructs the base state and an external disturbance wrench from proprioception alone — IMU and the leg kinematics of the settled stance feet — while the controller plans ground reaction forces inside friction cones over half a second of gait at 100 Hz and feeds the estimated disturbance forward. The robot ramps to a trot, absorbs a lateral push, and turns, with no ground-truth state anywhere in the loop. The report derives the model, gait, footholds and measurement model from first principles; the compiled real-time solvers substituted into the closed loop reproduce the reference behaviour without change.

- **Real-time-iteration NMPC and NMHE solvers** — ultra-fast solvers with state and input constraints, targeted at embedded control.
* **AEROFORGE — Autonomous aerial construction** — heterogeneous UAVs cooperatively assemble and verify a bridge using distributed estimation and real-time NMPC under cable, contact, wind, and actuator constraints.
- **Missile Guidance & Simulation** — 3-DOF
  3-DOF missile dynamics and guidance simulation covering trajectory propagation, aerodynamic effects, guidance laws, and interception scenarios.
- **Missile Guidance & Simulation** — 6-DOF
  Full 6-DOF rigid-body missile simulation using position, velocity, attitude/quaternion, and body-rate states, with aerodynamic forces/moments, thrust, gravity, control-surface effects, and guidance.
- **Hexacopter Simulation & Control in a Mars Rover mission** — ROS 2
  Six-rotor UAV simulation implemented in ROS 2, covering vehicle dynamics, attitude/position control, simulation integration, and the foundation for future sensor-fusion and autonomous-flight work.
- **Vehicle control basics lane assist using PID + MPC** in python (Udemy-updating)
- **Vehicle suspension control** - Nonlinear system linearization, State-space and Laplace analysis, Stability and pole analysis, Modal analysis, MIMO control, Pole placement, Vehicle suspension controller design,
  PID + LQR + Resonance analysis, Advanced vehicle suspension control using PID, LQR, resonance analysis, tuning with AI, and dominant pole approximation. (Udemy-updating)

- **Embedded validation** — I am also validating selected control, estimation and robotics projects on **Raspberry Pi**, moving algorithms from simulation to real embedded hardware and measuring their computational performance and real-time behaviour.

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
**Location** Nürnberg, Bavaria — open to relocation across Bavaria and Europe for the right role.

---

_The engineering decisions, algorithm and system design, validation strategy, analysis and stated limitations are my own._
