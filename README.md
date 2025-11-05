# DOPPLER-ONLY-TRACKING-IMPLEMENTATION

This project is the 2nd implementation assignment from the Estimation and Filtering course at Xi'an Jiaotong University (XJTU), implementing the paper "Extended Kalman Doppler tracking and model determination for multi-sensor short-range radar" by Mittermaier et al.

## Project Overview

This project implements a complete Doppler-only target tracking system using an Extended Kalman Filter (EKF) for short-range radar applications. The system estimates a target's 3D position and velocity using only Doppler shift measurements from multiple radar sensors, addressing the challenging nonlinear estimation problem inherent in frequency-based tracking.

## Key Features

- **Multi-Sensor Platform**: Circular array of 6 radar sensors with optimized spatial configuration
- **Nonlinear Estimation**: Extended Kalman Filter with analytical Jacobian computation
- **Robust Initialization**: Maximum Likelihood Estimation (MLE) for reliable filter bootstrap
- **Doppler Measurement Model**: Physics-based Doppler shift calculation for each sensor
- **3D Tracking**: Full 6-state estimation (position and velocity in 3D space)

## System Architecture

#### Core Components
- **Sensor Platform**: 6 radar sensors arranged in circular configuration (20cm radius)
- **Measurement Model**: Nonlinear Doppler equation with wavelength-dependent sensitivity
- **EKF Implementation**: Constant Velocity process model with proper noise characterization
- **MLE Initializer**: Batch optimization for initial state estimation

#### The Implementation
- State Vector: `[px, py, pz, vx, vy, vz]` (6-dimensional)
- Process Model: Constant Velocity 
