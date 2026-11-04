# RoboParty Meta-Packages (`roboparty_all`)

This repository provides a unified Debian metapackage designed to effortlessly install the complete RoboParty software stack. A metapackage does not contain code itself; instead, it declares dependencies on all the necessary sub-modules, allowing you to set up your entire robot environment with a single `apt install` command.

## Available Packages

* **`roboparty-all`**: The universal metapackage that applies to all RoboParty hardware platforms (including RoboPi1, RoboPi2, RoboPi3, and x86 development environments).

## Installed Components

Installing the metapackage will automatically pull in the latest versions of the following core modules via the APT dependency resolution:

* `roboparty-base` (Core runtime and rules)
* `roboparty-description` (URDF, Mesh, and MJCF models)
* `roboparty-bms` (Battery Management System drivers)
* `roboparty-imu` (IMU drivers)
* `roboparty-motors` (Motor controllers and interfaces)
* `roboparty-dexhand` (Dexterous hand driver)
* `roboparty-camera` (Camera drivers)
* `roboparty-inference` (AI inference capabilities)
* `roboparty-analyze` (Diagnostics and log analysis)
* `robopi-tui` (Configuration and diagnostics TUI)
* `roboparty-rp-server` (Unified web/WebSocket backend)
* `roboparty-start` (Runtime entry point and launch scripts)
* `roboparty-lidar` (Lidar driver placeholder)

The RP head packages are intentionally **not** part of this metapackage.
Install them explicitly when the target product needs them.

## Installation

Ensure you have added the `apt.roboparty.com` source to your system, then run:

```bash
sudo apt update
sudo apt install roboparty-all
```
