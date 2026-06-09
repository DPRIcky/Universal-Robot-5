# Introduction to Universal Robot 5 (UR5)

**Author:** Prajjwal Dutta  
**Affiliation:** Robotics and Autonomous Systems, Arizona State University, Arizona, USA

---

## Overview

This project documents hands-on lab work with the Universal Robots UR5 collaborative robotic arm. Labs cover three programming environments (Polyscope, RoboDK, URScript), workspace analysis, kinematics, gripper control, pick-and-place, and robotic assembly tasks.

---

## Table of Contents

- [Introduction & Programming Environments](#lab-1)
- [Gripper Control & Repeatability](#lab-2)
- [Gripper Tasks & Pick-and-Place](#lab-3)
- [Flashlight Assembly](#lab-4)
- [UR5 Specifications](#ur5-specifications)
- [Programming Environments Comparison](#programming-environments-comparison)

---

## Objective
Become familiar with the UR5 robot and operate it using Polyscope, RoboDK, and URScript. Final task: trace the 8 vertices of a virtual cube using linear motion commands.

### Task 1 – Waypoints in PolyScope

Moved the robot through 3 waypoints using both joint space and Cartesian space control.

| Pose   | X (mm) | Y (mm) | Z (mm) | RX (rad) | RY (rad) | RZ (rad) |
|--------|--------|--------|--------|----------|----------|----------|
| Pose 1 | -575   | -350   | 300    | 2.10     | 1.11     | 0.63     |
| Pose 2 | -240   | -445   | 650    | 1.57     | -1.57    | -1.57    |
| Pose 3 | 400    | -400   | 200    | 2.79     | -0.16    | 0        |

### Task 2 – RoboDK Simulation

- Imported the UR5 model with table station into RoboDK.
- Recorded 3 target positions and linked them to linear joint space movements.
- Validated simulation before deploying to the real robot.

### Task 3 – URScript

- Defined robot positions programmatically using URScript.
- Saved the script file in a format compatible with Polyscope.
- Executed the program on the real robot.

### Task 4 – Virtual Cube Tracing

The robot traced the 8 vertices of a virtual cube using `moveJ` (joint space) to reach the first corner, then `moveL` (linear) for all subsequent vertices.

| Point | X (mm)   | Y (mm)   | Z (mm) | RX (rad) | RY (rad) | RZ (rad) |
|-------|----------|----------|--------|----------|----------|----------|
| 1     | -140.07  | -609.05  | 424.95 | 3.080    | 0.585    | 0.035    |
| 2     | -140.06  | -659.00  | 424.98 | 3.080    | 0.585    | 0.035    |
| 3     | -90.03   | -658.96  | 425.01 | 3.080    | 0.585    | 0.035    |
| 4     | -90.04   | -608.98  | 425.01 | 3.080    | 0.585    | 0.035    |
| 5     | -140.07  | -609.05  | 424.95 | 3.080    | 0.585    | 0.035    |
| 6     | -90.05   | -609.02  | 324.98 | 3.080    | 0.585    | 0.035    |
| 7     | -140.05  | -609.00  | 324.96 | 3.080    | 0.585    | 0.035    |
| 8     | -140.09  | -658.98  | 324.97 | 3.080    | 0.585    | 0.035    |
| 9     | -90.04   | -658.97  | 325.02 | 3.080    | 0.584    | 0.035    |

**Cube Volume Calculation:**

Side length (Euclidean distance between diagonal corners, Points 1 and 6):
