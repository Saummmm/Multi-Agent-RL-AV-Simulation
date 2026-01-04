# Multi-Agent RL Intersection Simulation

This repository is a culmination of an exploration into simulating an intersection environment for the purposes of training a multi agent model for the purposes of autonomous transportation. The simulation environemnt uses Farama Foundation's highway-env. Then it also uses AgileRL's MATD3 as a model to be trained. Because of the environment used, Google Colab, the training method had to be batched per step. The model was trained for a total of 2,000,000 steps, which took much longer than the time limit on a run environemnt for google colab. So, after every 100,000 steps, the model was saved to preserve the previous weights that had been allocated. The test_runs directory shows a log of a test run of each model segment including the observations, rewards and episode frames.

---

## Repository Structure

Multi-Agent-RL-AV-Simulation/
- MultiAgent_RL_Intersection_Simulation.ipynb
- test_runs/
- README.md


### File Descriptions

- **MultiAgent_RL_Intersection_Simulation.ipynb**  
  Main notebook containing:
  - Dependency installation
  - Environment and agent setup
  - Multi-agent training loops
  - Checkpointing and chunked training
  - Visualization and result generation

- **test_runs/**  
  Directory used to store saved agents, checkpoints, and outputs generated during testing runs.

---

## Environment and Frameworks

The simulation is built using the following frameworks and libraries (as imported in the notebook):

- **AgileRL**
  - MATD3
  - Tournament selection and mutation utilities
- **PettingZoo**
  - Parallel multi-agent environment interface
- **Gymnasium**
  - Environment and space definitions
- **Highway-Env**
  - Traffic and autonomous driving simulation environment
- **PyTorch**
  - Neural network implementation
- **NumPy / Matplotlib**
  - Data handling and visualization

The notebook is configured to run in a **Linux environment** and was executed using **Google Colab** due to resource requirements. Compute engine used was a high-ram CPU.