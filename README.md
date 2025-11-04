# SaVILA：Safe-Robot-Vision-Language-Action-System-for-Navigation
A hierarchical framework enabling robots to navigate unknown environments via natural language, addressing collision collision issues of existing VLA systems.

## Overview
SaVILA is a hierarchical navigation framework enabling robots to safely navigate unknown environments via natural language instructions. It addresses collision risks in existing Vision-Language-Action (VLA) systems by integrating high-level semantic reasoning with low-level safe motion control, delivering robust performance in simulations and real-world scenarios.


## Core Principle
SaVILA uses a two-layer architecture to balance semantic understanding and collision-free motion:
- **High-Level Semantic Reasoning**: A fine-tuned vision-language model processes RGB images and natural language instructions to generate mid-level motion commands (e.g., "turn 45° left and move forward 2m") at low frequency, focusing on high-level navigation intent.
- **Low-Level Safe Control**: A real-time, point-cloud-driven motion policy (based on neuro-symbolic optimization) executes these commands, ensuring collision avoidance and dynamic feasibility using raw LiDAR data, operating at high frequency for responsive control.


## Key Features
- **Superior VLN Performance**: Outperforms state-of-the-art methods by >9% on standard benchmarks (e.g., 51.2% success rate on R2R Val-Unseen) with only RGB inputs.
- **Strong Spatial Reasoning**: 2.1m relative distance error and 0.86° orientation error (20-27% lower than prior models) on a self-collected dataset.
- **Robust Obstacle Avoidance**: 93% success rate with 7% collision rate in dynamic environments (outperforming RL-based methods).
- **Cross-Platform Adaptability**: Deployed on Unitree Go2 (quadruped), H1 (humanoid), and Booster T1 (wheeled exoskeleton).
- **Extensible Interaction**: Integrates with voice systems (e.g., "Xiaozhi") for conversational command execution, suitable for service/assistive robotics.


## Experimental Results
- **Simulations**: 8% higher success rate in Habitat-Ir-Sim co-simulations compared to other obstacle avoidance strategies.
- **Real-World**: 90% indoor and 85% outdoor success rates, significantly outperforming baseline models.


## References & Related Projects
- [Habitat Simulator](https://aihabitat.org/) (Simulation environment)
- [VILA](https://github.com/facebookresearch/vila) (Vision-language foundation model)
- [NaVILA](https://arxiv.org/abs/2403.14493) (Related VLN framework)
- [Fast-LIO2](https://github.com/hku-mars/FAST_LIO) (LiDAR odometry for real-world deployment)


## Code Release
Code is currently under preparation and is scheduled to be released in **Q2 2026**. The repository will include:
- Training/evaluation scripts for the VLA model
- Motion control policy implementation
- Simulation configurations (Habitat/Ir-Sim)
- Example datasets and deployment guides


## Contact
For questions, please reach out to [your-email@example.com].

---
*Paper reference: [To be updated upon publication]*
