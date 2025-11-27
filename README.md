# Experiences-of-using-Reinforcement-Learning-in-the-context-of-Automation-Engineering
Bachelor Thesis - Reinforcement Learning in the context of Automation Engineering

**Bachelor Thesis Project** - Bachelor's Degree in Computer and Automation Engineering  
**University:** Università Politecnica delle Marche  
**Author:** Alessandro Binci  
**Language:** Italian
**Supervisor:** Prof. Domenico Ursino  
**Year:** 2022-2023

📄 **[Read the Full Thesis (PDF)](docs/Binci_Alessandro_Bachelor_Thesis.pdf)**

---

## Project Overview

This project investigates the application of **Deep Reinforcement Learning (DRL)** algorithms to solve complex control and automation problems in industrial and robotic contexts. 

The study focuses on the intersection of **Industry 4.0** paradigms and Machine Learning, demonstrating how intelligent agents can learn optimal control policies through trial-and-error interactions with dynamic environments. The experimental phase involves the design, training, and validation of RL agents in **MATLAB & Simulink** environments.

## Case Studies

The research is validated through three distinct simulation scenarios, each addressing a specific control challenge using state-of-the-art DRL algorithms.

### 1. Robot Arm Balance (Manipulation)
* **Objective:** Train a robotic manipulator (Kinova Gen3) to balance a ball on a plate attached to its end-effector.
* **Algorithm:** **SAC (Soft Actor-Critic)**.
* **Challenge:** Continuous control with high sensitivity to initial conditions.
* **Outcome:** The agent successfully learned to stabilize the ball, optimizing the trade-off between exploration and exploitation (Entropy Regularization).

### 2. Automatic Parking Valet (Automotive)
* **Objective:** Enable an ego-vehicle to autonomously park in a target spot avoiding obstacles.
* **Algorithm:** **TD3 (Twin-Delayed DDPG)** combined with **MPC (Model Predictive Control)**.
* **Challenge:** Hybrid control architecture where MPC handles trajectory tracking and RL handles the final parking maneuver in a constrained space.
* **Outcome:** Comparison of different neural network architectures (layer depth) to improve convergence speed and path accuracy.

### 3. Bipedal Walking Robot (Locomotion)
* **Objective:** Train a bipedal robot to walk in a straight line.
* **Algorithms:** Comparison between **DDPG (Deep Deterministic Policy Gradient)** and **TD3**.
* **Challenge:** High-dimensional state space and unstable dynamics (falling risk).
* **Outcome:** Comparative analysis showed that TD3 provides greater learning stability and smoother control policies compared to standard DDPG.

---

## Technologies & Tools

* **Environment:** MATLAB R2023b / Simulink
* **Toolboxes:** * Reinforcement Learning Toolbox
    * Simscape Multibody (for physical modeling)
    * Automated Driving Toolbox (for the parking scenario)
* **Algorithms:** SAC, DDPG, TD3

---

## Key Results

The project highlights the critical role of **Hyperparameter Tuning** in DRL. The extensive experimental phase demonstrated that:
* **Discount Factor ($\gamma$):** Crucial for stability in continuous tasks (e.g., robot walking).
* **Network Architecture:** Deeper networks provided better generalization in the parking scenario but required careful regularization to avoid overfitting.
* **Algorithm Selection:** TD3 proved superior to DDPG in locomotion tasks, significantly reducing the overestimation bias of Q-values.

---

## Repository Structure

* `docs/`: Contains the full thesis PDF and related documentation.
* `src/RobotArm/`: MATLAB scripts and Simulink models for the SAC experiment.
* `src/ParkingValet/`: MATLAB scripts and Simulink models for the TD3/MPC experiment.
* `src/WalkingRobot/`: MATLAB scripts and Simulink models for the DDPG vs TD3 comparison.

## References
All references are available in the thesis bibliography above.
