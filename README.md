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

### Isaac Sim

The simulation demonstrations serve two complementary validation purposes: checking whether a generated assembly sequence remains feasible as the product is progressively assembled, and visualizing the local mating motions used to realize individual assembly steps.

#### Sequence Feasibility Validation

Representative sequence-level simulations for products from the Manual2Skill++ benchmark.

| SUNDVIK | VASSKAR |
| :---: | :---: |
| <img src="media/isaac_sim/sundvik_15sec.gif" width="100%"> | <img src="media/isaac_sim/vasskar_6sec.gif" width="100%"> |

#### Mating Motion Simulation

Representative local assembly-motion simulations showing how planned mating operations are executed in Isaac Sim.

| Desk | Round Table |
| :---: | :---: |
| <img src="media/isaac_sim/desk_assembly_17sec.gif" width="100%"> | <img src="media/isaac_sim/round_table_assembly_7sec.gif" width="100%"> |

### Physical Robot Execution

A representative hardware demonstration showing transfer of planned assembly motion from the reasoning and simulation workflow to a physical robot system.

<p align="center">
  <img src="media/robot/robot_implementation_6sec.gif" width="70%">
</p>

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

At this stage, the repository contains only material suitable for public portfolio presentation. Research source code and detailed methodology will remain private while the manuscript is under review.

## Publication

Publication information and a formal citation will be added after the associated manuscript reaches an appropriate public status.

## Contact

For research or collaboration inquiries, please use the contact information provided on my GitHub profile.
