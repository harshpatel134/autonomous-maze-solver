# Autonomous Maze Solver Robot

## Overview

An autonomous maze-solving robot designed and built for maze navigation competitions.

The robot uses a Teensy 4.1 as the main controller, multiple VL53L1X ToF sensors for wall detection, a BNO085 IMU for accurate turning, and encoder-driven motors with PID-based motion control.

## Competition Achievements

- 🥇 2nd Rank — Mindbend Autonomous Maze Solver Competition, SVNIT
- 🏆 8th Rank in the Ideation Round — Robofest Gujarat 5.0 (GUJCOST)
- Advanced to the Proof-of-Concept (PoC) stage at Robofest Gujarat 5.0

## Hardware

| Component | Purpose |
|---|---|
| Teensy 4.1 | Main controller |
| 5× VL53L1X ToF Sensors | Wall and distance detection |
| BNO085 9-Axis IMU | Orientation and turn control |
| TCA9548A I2C Multiplexer | Managing multiple ToF sensors |
| N20 12V 300RPM Encodered Motors | Robot movement and feedback |
| MC33926 Motor Driver | Motor control |
| Custom 2-Layer Acrylic Chassis | Robot mechanical structure |

## Algorithms

### Wall Following

A wall-following algorithm is used for maze exploration and mapping.

### PID-Based Corridor Centering

The robot calculates the difference between the left and right wall distances:

```text
Error = distance_L - distance_R
