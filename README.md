# Adaptive Traffic Light Optimization using Reinforcement Learning

An intelligent traffic signal control system built using **Deep Q-Learning (DQN)** and **SUMO (Simulation of Urban Mobility)**.  
This project dynamically adjusts traffic light phases based on real-time traffic conditions, reducing congestion and improving traffic flow.

---

## Project Overview

Traditional traffic lights follow fixed timers, which often cause unnecessary waiting and traffic jams.  
This project implements an **adaptive traffic light controller** that learns optimal signal timing using **Reinforcement Learning (RL).**

The agent observes:
- Lane vehicle counts  
- Queue lengths  
- Traffic density  

And decides:
- When to switch signals  
- When to extend green  
- How long each phase should remain active  

---

## Key Features

- **Deep Q-Network (DQN)** based learning  
- **SUMO** real-time traffic simulation  
- Custom **Gym-like RL environment**  
- Reward based on **queue reduction & waiting time**  
- Adaptive phase switching  
- Clean & reproducible project suitable for **GitHub, Resume, LinkedIn**

---

##  Project Structure

```
adaptive-traffic-rl/
│── environment/
│     ├── traffic_env.py
│     ├── utils.py
│
│── training/
│     ├── dqn_agent.py
│     ├── train.py
│
│── models/
│     └── saved_model.h5
│
│── sumo/
│     ├── network.net.xml
│     ├── route.rou.xml
│
│── requirements.txt
│── README.md
│── run_simulation.py
```

---

## Technologies Used

- Python  
- SUMO  
- Reinforcement Learning (DQN)  
- NumPy / Pandas  
- TensorFlow / Keras  
- TraCI API  

---

#  How to Run the Project

Follow these steps to install SUMO, install dependencies, train the agent, and run the simulation.

---

#  1. Install SUMO (Mandatory)

### Windows Installation
1. Download SUMO from:  
   https://sumo.dlr.de/releases/
2. Install the **-win64** version
3. Add SUMO to PATH:  
   - Open **“Edit the system environment variables”**  
   - Under *System Variables* → open **Path**  
   - Add this path:
     ```
     C:\Program Files (x86)\Eclipse\Sumo\bin
     ```

### Verify SUMO Installation
```bash
sumo --version
```

---

# 2. Install Python Dependencies

Install required libraries:

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install numpy pandas torch matplotlib
pip install sumolib traci
```

---

# 3. Train the RL Agent (DQN)

```bash
python training/train.py
```

This will:
- Launch SUMO simulation  
- Train the DQN agent  
- Save model into **models/**  

---

# 4. Run / Test the Simulation

```bash
python run_simulation.py
```

This will:
- Load the trained DQN model  
- Start SUMO GUI  
- Show adaptive traffic signal control  

---

# Reward Function Logic

The reward encourages the agent to:

- Reduce waiting time  
- Minimize queue length  
- Improve overall traffic flow  

### Formula:
```python
reward = -(waiting_time + queue_length)
```

---

# Results (Example)

- **25–40% decrease** in average vehicle waiting time  
- Smoother traffic flow  
- Better handling of traffic spikes  

---

# Use Cases

- Smart city traffic management  
- Intelligent transportation systems  
- Urban traffic planning  
- AI research with SUMO  

---

