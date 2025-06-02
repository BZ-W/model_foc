# model_foc

`model_foc` is a fixed-point, discrete-time Field-Oriented Control (FOC) Simulink model for Permanent Magnet Synchronous Motor (PMSM), incorporating an Extended Kalman Filter (EKF) observer. The model supports C code generation as a Simulink S-Function via MINGW, and is intended for algorithm validation and simulation in motor control systems.

## Project Overview

This project is developed in MATLAB Simulink (R2024b) and targets sensorless PMSM control applications. It integrates an EKF-based rotor position and speed estimator and implements a fixed-point FOC controller structure. The model is simulation-ready and supports local S-Function generation for acceleration or integration with higher-level systems.

## Features

- Fixed-point implementation of FOC control structure
- Discrete-time EKF observer (current input, angle/speed output)
- Simulink-based simulation environment with fixed-step solver support
- Local S-Function generation using Simulink Coder and MINGW-w64
- Single .slx model file, directly executable

## System Requirements

- MATLAB R2024b
- Simulink
- Fixed-Point Designer
- Simulink Coder
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
├── foc_sim.slx       # Simulink model: fixed-point FOC + EKF for PMSM
└── README.md         # Project documentation
```

## Applications

- Sensorless PMSM control algorithm development
- Fixed-point FOC structure validation
- EKF-based observer simulation and analysis
- Control education and model-based algorithm prototyping

## Author

BZ

## License

This project is dual-licensed under the following open-source licenses. You may choose the license that best suits your use case:

- [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
- [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.html)

Please retain the original author attribution and license notice when using or modifying this project.
