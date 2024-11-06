# RL-CIA
MAB Recommender System and MDP 

## CIA 1:
## Multi-Armed Bandit Movie Recommendation System

A simple movie recommendation system built using the **Multi-Armed Bandit (MAB)** approach with the **epsilon-greedy algorithm**. The system is designed to make recommendations based on user feedback, learning over time to balance between exploration (trying new movies) and exploitation (recommending movies that tend to have high ratings).

<br/>

## Dataset

The recommendation system uses the [MovieLens 100K dataset](https://grouplens.org/datasets/movielens/100k/), a widely-used public dataset in recommendation system research. It contains 100,000 ratings from 943 users on 1,682 movies, making it suitable for experimenting with various recommendation algorithms.

<br/>

## Methodology

The code implements an **epsilon-greedy** strategy, where:
- With probability `epsilon`, the system randomly recommends a movie to explore new options.
- With probability `1 - epsilon`, the system recommends the movie with the highest estimated reward (expected rating), allowing it to exploit known high-performing options.

The system adapts dynamically, improving recommendations as more user feedback is received.


--- 

<br/>

## CIA 2:
## Reinforcement Learning on a 100x100 Grid with Obstacles
# Overview
This project demonstrates the use of reinforcement learning (RL) and dynamic programming (DP) techniques to navigate a grid environment with obstacles. The environment consists of a 100x100 grid where an agent must find the optimal path from a start point to a goal point, avoiding obstacles placed randomly in the grid.

# Objectives
Grid Environment: Create a 100x100 grid with a defined start and goal position, and randomly placed obstacles.
Dynamic Programming (DP): Implement Value Iteration to compute the optimal policy and value table.
Reinforcement Learning (RL): Use Q-learning to find the optimal path from start to goal.
Benchmarking: Compare the performance of Value Iteration and Q-learning in terms of path efficiency and steps taken.
---
<br/>

# Project Structure

1. Environment Setup
A grid is initialized with start and goal points, and obstacles are randomly placed. The grid states are defined as follows:
0: Free cell
1: Obstacle
2: Start
3: Goal


2. MDP Setup
The environment is framed as a Markov Decision Process (MDP) with the following components:
States: Each cell in the grid, represented by its coordinates.
Actions: Four possible moves—up, down, left, and right.
Rewards: Reaching the goal yields a large positive reward, hitting obstacles incurs a penalty, and each step has a small penalty to encourage efficient paths.


3. Value Iteration (Dynamic Programming)
Value Iteration is used to compute the optimal value for each state iteratively. Using a discount factor, the algorithm updates the value of each state based on the potential rewards of moving to neighboring states.


4. Q-Learning (Reinforcement Learning)
Q-learning, a model-free RL algorithm, is used to learn an optimal policy through trial and error. An epsilon-greedy policy balances exploration and exploitation, where the agent either explores random actions or exploits the current best action based on Q-values.



5. Benchmarking and Evaluation
The DP policy is evaluated by measuring the steps taken to reach the goal, and the results are compared against the RL-based Q-learning solution.
