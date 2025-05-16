# Reinforcement-Learning
IMBIZO PROJECT 2022

# Dyna‑Q vs. Model‑Free Q‑Learning in a Gridworld

## Overview  
This project explores and compares a model‑free Q‑Learning agent with a model‑based Dyna‑Q agent navigating a gridworld containing obstacles. The Dyna‑Q agent combines real experience with simulated “planning” steps drawn from its learned transition model.

## Implementation  
- **Environment:**  
  - Custom 2D gridworld with walls/obstacles  
  - Start and goal states defined  
- **Agents:**  
  - **Model‑Free Q‑Learning:** Updates Q‑values only from real experience  
  - **Dyna‑Q (Model‑Based):**  
    1. Learns a transition/reward model from experience  
    2. Performs _n_ simulated planning steps per real step to update Q‑values  
- **Experiments:**  
  - Navigation performance with static obstacles  
  - Direct comparison of learning curves (reward vs. episode)  
  - Varying planning steps (_n_ = 2, 5, 10) to measure impact on learning speed  

## Results  
- **Learning Speed & Performance:**  
  - Dyna‑Q converges faster and achieves higher cumulative reward than pure Q‑Learning.  
  - More planning steps (_n_ = 10) yield the best performance gains.  
- **Visualizations:**  
  - Heatmaps of Q‑values over episodes for both agents  
  - Reward‑per‑episode plots showing convergence rates  
  - Comparison of trajectories learned in obstacle regions  

## How to Run  
1. Clone this repo  
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
