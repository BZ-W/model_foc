# model_foc

`model_foc` is a discrete-time Field-Oriented Control (FOC) Simulink model for Permanent Magnet Synchronous Motor (PMSM), incorporating an Extended Kalman Filter (EKF) observer. The model is designed for simulation and algorithm verification and supports C code generation as a Simulink S-Function using MINGW.

## Project Overview

This project is developed in MATLAB Simulink (R2024b) and targets sensorless PMSM control applications. It integrates an EKF-based rotor position and speed estimator and implements a discrete-time FOC controller structure using a fixed-step solver. The model is simulation-ready and supports local S-Function generation for acceleration or integration into larger systems.

## Features

- Discrete-time implementation of FOC control structure for PMSM
- EKF observer using current input to estimate rotor angle and speed
- Simulink-based simulation environment with fixed-step solver
- S-Function C code generation supported via Simulink Coder and MINGW-w64
- Single .slx model file, directly executable

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

2. Launch MATLAB and open the model:

    ```matlab
    open_system('foc_sim.slx');
    ```

3. Run the simulation in Simulink or use Simulink Coder to generate the corresponding S-Function.

## Repository Structure

```
model_foc/
├── foc_sim.slx       # Simulink model: discrete-time FOC + EKF for PMSM
└── README.md         # Project documentation
```

## Applications

- Sensorless PMSM control algorithm development
- Discrete-time FOC structure validation
- EKF-based observer simulation and analysis
- Control education and model-based design verification

## Author

BZ

## License

This project is dual-licensed under the following open-source licenses. You may choose the license that best suits your use case:

- [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
- [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.html)

Please retain the original author attribution and license notice when using or modifying this project.
