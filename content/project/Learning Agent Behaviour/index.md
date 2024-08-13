---
title: Learning Agent Behavior
summary:  Implemented DAGGER and Reinforce to learn an optimal policy in Hopper-v4 and Ant-v4 environments from OpenAI Gym
tags:
  - Deep Learning
date: '2024-04-01'

# Optional external URL for project (replaces project detail page).
external_link: ''

# image: 
#   caption: Plots of actual, observed and estimated trajectory
#   focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/shubhgoel20/COL778_Autonomous_Systems/tree/main/A4
  - icon: :arrow_forward:
    icon_pack: emoji
    name: Ant-v4
    url: 'uploads/ant.mp4'
url_code: ''
url_pdf: ''
url_slides: ''
url_video: 'uploads/feature.mp4'
url_video: 'uploads/ant.mp4'

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ''
---
Team-Shubh Goel (2020EE10672) & Chinmay Mittal (2020CS10336)

## Part-1: Imitation Learning

- We implemented the DAGGER algorithm
- We first select the policy (agent or expert) with some probablility beta, which would be used for sampling trajectories for DATA augmentation
- Using the selected policy we sample T_step trajectories for data augmentation
- We then get the expert actions on the sampled trajectories and add them to the replay buffer
- We then train our agent's policy network in the following way:
  - We first sample 100 batches of batch size 256 from the replay buffer.
  - We then train the model on the above batches for 10 epochs

## Part-2: Reinforcement Learning (Policy Gradients)

- We implemented the vanilla REINFORCE algorithm.
- We first sample multiple trajectories given the current policy network till the goal.
- For each trajectory we then compute the discounted reward to go from each state.
- We then compute the gradient of the policy network by taking the dot product of the log of the probability of the action given the state and the reward to go.
- The policy network predicts the mean of the action distribution given the state, and we also learn the standard deviation of the action distribution as another parameter.
- We model the action distribution given the state as a Gaussian distribution.
- In each training iteration we do a single update to the policy network.
- To further stabilise training we subtract the baseline from the reward vector which is computed as the average reward to go.

## Part-3: State of the art RL techniques

- We tried the following SOTA techniques - PPO, SAC, DDPG, TD3
- TD3 worked best for the Ant environment and SAC worked the best for the PnadaPush environment
- We used Hindsight Experience Replay (HER) to deal with sparse reward problem for PandaPush environment.
