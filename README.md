# model_foc

`model_foc` is a discrete-time Field-Oriented Control (FOC) Simulink model for Permanent Magnet Synchronous Motor (PMSM), incorporating an Extended Kalman Filter (EKF) observer. The model is intended for simulation and algorithm verification, with system parameters generated via a preparatory MATLAB Live Script.

## Project Overview

This project is developed in MATLAB Simulink (R2024b) and targets sensorless PMSM control applications. It integrates an EKF-based rotor position and speed estimator within a discrete-time FOC framework using a fixed-step solver. The model includes a parameter initialization script (`Para_Gen.mlx`) that must be executed prior to running the Simulink model.

The model supports local C code generation as a Simulink S-Function via MINGW for acceleration or integration into larger systems.

## Features

- Discrete-time implementation of FOC for PMSM with fixed-step solver
- EKF observer using current feedback to estimate rotor angle and speed
- MATLAB Live Script for parameter generation (`Para_Gen.mlx`)
- Compatible with Simulink Coder and MINGW-w64 for S-Function generation
- Structured, simulation-ready workflow

## System Requirements

- MATLAB R2024b
- Simulink
- Simulink Coder (for S-Function generation)
- MINGW-w64 (configured via `mex -setup`)

> Note: This model is not intended for embedded target deployment. Generated code is for local S-Function use only.

## Quick Start

1. Clone the repository:

    ```bash
    git clone https://github.com/BZ-W/model_foc.git
    cd model_foc
    ```

2. Launch MATLAB and run the parameter generation script:

    ```matlab
    run('Para_Gen.mlx');
    ```

3. Open and simulate the model:

    ```matlab
    open_system('foc_sim.slx');
    ```

4. Optionally, generate S-Function using Simulink Coder for acceleration or integration.

## Repository Structure

```
model_foc/
├── foc_sim.slx       # Simulink model: discrete-time FOC + EKF for PMSM
├── Para_Gen.mlx      # MATLAB Live Script for system parameter generation
└── README.md         # Project documentation
```

## Applications

- Sensorless PMSM control algorithm development
- Discrete-time control structure validation
- EKF observer simulation and performance evaluation
- Algorithmic prototyping and teaching in control engineering

## Author

BZ

## License

This project is dual-licensed under the following open-source licenses. You may choose the license that best suits your use case:

- [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
- [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.html)

Please retain the original author attribution and license notice when using or modifying this project.
