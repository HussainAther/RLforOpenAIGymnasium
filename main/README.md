# Reinforcement Learning for OpenAI Gymnasium LunarLander-v2

Welcome to the repository for the Reinforcement Learning project focused on solving the OpenAI Gymnasium LunarLander-v2 environment.

## Project Overview

This project aims to develop reinforcement learning algorithms to solve various OpenAI Gym environments, starting with Gymnasium's LunarLander-v2 environment. The objective is to train an AI agent to navigate and land a lunar module safely on the surface of the moon while maximizing the reward. Traditional reinforcement learning techniques often face challenges with sparse feedback, hindering efficient adaptation to changing environments. This project explores the incorporation of additional intrinsic rewards based on state visitation frequency to enhance the feedback loop.

## Project Structure

The project follows a structured approach, including the following components:

1. **Problem Identification:** Formulation of problem statement, context, criteria for success, scope of solution space, constraints, stakeholders, and data sources.
2. **Data Wrangling:** Data exploration and preparation, utilizing simulated sensor data from the LunarLander-v2 environment provided by OpenAI Gymnasium.
3. **Exploratory Data Analysis:** Visualization and analysis of observations, rewards, and actions using Gymnasium's built-in functionalities.
4. **Pre-processing and Training Data Development:** Pre-processing observations and splitting data into training, validation, and test sets.
5. **Modelling:** Selection and implementation of reinforcement learning algorithms (e.g., Q-learning, Deep Q-Networks, Policy Gradient methods), training the AI agent, and evaluation of performance.
6. **Documentation:** Creation of a comprehensive project report, including problem formulation, methodology, results, and discussion. Additionally, clear and concise documentation for the codebase will be provided, including comments and explanations.
7. **Deliverables:** GitHub Repository containing code for each step of the project, a slide deck summarizing project objectives and results, and a project report detailing problem formulation, methodology, results, and discussion.

This project implements the [LunarLander-v2](https://gym.openai.com/envs/LunarLander-v2/) from OpenAI's Gym with Pytorch. The goal is to land the lander safely in the landing pad with the Deep Q-Learning algorithm.

### Introduction

Landing pad is always at coordinates `(0,0)`. Coordinates are the first two numbers in state vector. Reward for moving from the top of the screen to landing pad and zero speed is about `100..140` points. If lander moves away from landing pad it loses reward back. Episode finishes if the lander crashes or comes to rest, receiving additional `-100` or `+100` points. Each leg ground contact is `+10`. Firing main engine is `-0.3` points each frame. Solved is `200` points. Landing outside landing pad is possible. Fuel is infinite, so an agent can learn to fly and then land on its first attempt. Four discrete actions available: do nothing, fire left orientation engine, fire main engine, fire right orientation engine.


## Getting Started

To get started with the project, follow these steps:

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/HussainAther/RLforOpenAIGymnasium.git
   ```
2. Install the necessary dependencies listed in the `requirements.txt` file:
   ```bash
   pip install -r requirements.txt
   ```
3. Explore the project structure and documentation to understand the methodology and implementation details.
4. Run the provided code scripts and notebooks to reproduce the experiments and results.

## Feedback and Contributions

Feedback, suggestions, and contributions are welcome! If you have any ideas for improving the project or would like to contribute to its development, please open an issue or submit a pull request.

## References

- ["Signal Novelty Detection as an Intrinsic Reward for Robotics"](https://www.mdpi.com/1424-8220/23/8/3985)

## License

This project is licensed under the [MIT License](LICENSE).
