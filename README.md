# Connector-Aware Robotic Assembly

A geometry-aware robotic assembly framework that reasons from **individual CAD/mesh parts** to generate assembly plans, validate assembly motions in **NVIDIA Isaac Sim**, and transfer validated motions to a **physical robot system**.

> **Research status:** The associated manuscript is currently under review. This repository is intentionally maintained as a **project showcase**; implementation details, source code, decision rules, thresholds, and other unpublished methodological details are withheld until the work is appropriate for public release.

## System Overview

The project connects part-level geometry to executable robotic assembly through the following high-level workflow:

```text
Individual CAD / Mesh Parts
            ↓
Connector-Aware Assembly Reasoning
            ↓
Assembly Planning
            ↓
Pose & Motion Generation
            ↓
Isaac Sim Validation
            ↓
Physical Robot Execution
```

Rather than assuming a fully assembled product model or a pre-defined mating sequence, the workflow builds an assembly plan from available part geometry, generates assembly poses and motions, checks the resulting sequence in simulation, and uses the validated motion information for robot execution.

The public showcase intentionally does **not** disclose the unpublished internals of connector extraction, compatibility rules, configuration generation or ranking, pose construction, sequence search, numerical thresholds, or detailed experimental results.

## Project Highlights

- **Geometry-first assembly reasoning** from individual CAD/mesh parts.
- **Connector-aware planning** for inferring physically meaningful part relationships.
- **Assembly pose and motion generation** for insertion and fastening-style operations.
- **Sequence-level validation** before physical execution.
- **NVIDIA Isaac Sim** for assembly-sequence and mating-motion simulation.
- **Physical robot demonstrations** for validating transfer from planning and simulation to hardware.

## Demonstrations

### Isaac Sim — Assembly Sequence & Mating Motions

Simulation videos demonstrate generated assembly sequences and local mating motions in NVIDIA Isaac Sim. These visualizations are used to inspect assembly feasibility and motion consistency before robot execution.

<!--
Add public Isaac Sim videos here after upload.
Suggested location: media/isaac_sim/
-->

### Physical Robot Execution

Physical demonstrations show representative assembly motions executed on robot hardware using the planned and simulation-validated motion information.

<!--
Add public robot videos here after upload.
Suggested location: media/robot/
-->

## Technology

- **Python**
- **NVIDIA Isaac Sim**
- **USD / PhysX simulation workflow**
- **CAD and mesh geometry processing**
- **OpenCV / visualization utilities**
- **Robot kinematics and coordinate transformations**
- **Robotic assembly planning and validation**

## Research Direction

The broader goal is to reduce the amount of product-specific structure that must be supplied in advance for robotic assembly. The project investigates how geometric information available at the part level can be composed into assembly hypotheses and then connected to simulation and physical execution.

## Repository Contents

At this stage, the repository contains only material suitable for public portfolio presentation.

```text
README.md        Project overview and high-level system architecture
media/           Public simulation and robot demonstrations (to be added)
```

Research source code and detailed methodology will remain private while the manuscript is under review.

## Publication

Publication information and a formal citation will be added after the associated manuscript reaches an appropriate public status.

## Contact

For research or collaboration inquiries, please use the contact information provided on my GitHub profile.
