# RAMP-RT Dataset

**Rocket, Artillery, and Mortar Projectile Radar Targets**

**Overview**

The RAMP-RT dataset (Rocket, Artillery, Mortar Projectiles – Radar Targets) provides synthetic radar detections and state estimates for ballistic trajectories generated using a point-mass model. Each trajectory corresponds to a specific projectile class (e.g., ML, MM, MH, GL, GH, RL, RM, RH), covering a broad range of calibers and dynamic regimes typical of battlefield projectiles.

**Data Generation**

All trajectories were simulated using a point-mass model with gravity and aerodynamic drag. The radar detections (range, azimuth, elevation) were synthetically generated to emulate a typical Weapon Locating Radar (WLR) ( or Firefinder Radar or Counter-Battery Radar) operating scenario. Measurement noise was added according to realistic sensor parameters (e.g., SNR, angular and range noise).

The state estimation for each trajectory was performed using the Square-Root Cubature Kalman Filter (SR-CKF), without prior knowledge of the ballistic coefficient. Thus, the dataset provides estimated parameters derived directly from radar measurements.

**Dataset Contents**

Each record includes:

Class label (projectile type)

Estimated kinematic parameters (from SR-CKF)

RCS statistics (mean and maximum scatter difference)

**Intended Use**

RAMP-RT is designed for research in:

Radar signal processing and filtering

Machine learning classification of ballistic projectiles

Estimation and tracking of launch/impact points

Dataset generation and benchmarking in counter-battery radar applications

Example applications

Training and validation of classifiers distinguishing rockets, artillery, and mortar projectiles based on estimated dynamics.

Benchmarking of Kalman filter variants under uncertain aerodynamic conditions.

Fusion of synthetic radar detections with RCS features for integrated classification and estimation pipelines.

**Citation**

If you use RAMP-RT in your research, please cite it as:
How to cite:
@misc{ramp-rt2025,
 title = {RAMP-RT: Rocket, Artillery, and Mortar Radar Targets Dataset},
 author = {Crus, D. M. O.},
 year = {2025},
 howpublished = {GitHub repository, https://github.com/DanielMinan/RAMP-RT}
}

**Contact**
For questions or requests (access to raw logs, provenance details, endorsement for use in publications): [minan.daniel@ime.eb.br]
