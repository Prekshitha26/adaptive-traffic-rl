Adaptive Traffic Light Optimization using Reinforcement Learning (DQN + SUMO)

An intelligent traffic signal control system built using Deep Q-Learning (DQN) and SUMO (Simulation of Urban MObility).
This project dynamically adjusts traffic light phases based on real-time traffic conditions, reducing congestion and improving traffic flow.

--Project Overview
Traditional traffic lights follow fixed timers, which often cause unnecessary waiting and congestion.
This project implements an adaptive traffic light controller that learns the optimal timing using Reinforcement Learning (RL).

The agent observes:
Lane vehicle counts
Queue lengths
Traffic density

And decides:
When to change the traffic signal
When to keep it green
How long each phase should stay active

--Key Features

 Deep Q-Network (DQN) based learning
 SUMO real-time traffic simulation
 Custom Gym-like RL environment
 Reward based on queue length reduction
 Adaptive phase switching
 Fully reproducible project for GitHub/Resume

--Project Structure
adaptive-traffic-rl/
│── environment/
│     ├── traffic_env.py
│     ├── utils.py
│── training/
│     ├── dqn_agent.py
│     ├── train.py
│── models/
│     └── saved_model.h5
│── sumo/
│     ├── network.net.xml
│     ├── route.rou.xml
│── requirements.txt
│── README.md
│── run_simulation.py

--Technologies Used
Python
SUMO
Reinforcement Learning (DQN)
NumPy / Pandas
TensorFlow / Keras
TraCI API

--How to Run the Project
1. Install Dependencies
pip install -r requirements.txt

2. Install SUMO (mandatory)
Download from: https://eclipse.dev/sumo/
Add SUMO to PATH:
setx SUMO_HOME "C:\Program Files (x86)\Eclipse\Sumo"

3. Train the Model
python training/train.py

4. Run Simulation
python run_simulation.py
--Reward Function Logic
The reward encourages the model to:
reduce waiting time
minimize queue length
improve flow efficiency

Reward is calculated as:
reward = -(waiting_time + queue_length)

--Results (Example)
25–40% decrease in average vehicle waiting time
Smoother intersection flow
Adaptive response to traffic spikes

--Use-Cases
Smart City traffic management
Intelligent transportation systems
Urban planning simulations
AI research using SUMO
