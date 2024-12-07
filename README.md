# Energy-Efficiency-and-Optimization-in-5g
Reduces energy consumption but also ensures sustainable and cost-effective network operations. 
## Overview

This project implements a reinforcement learning (RL) solution to optimize energy consumption in 5G networks. By dynamically switching between operational modes—**Normal Mode** and **Power-Saving Mode**—based on traffic load, the system ensures energy-efficient performance without compromising network reliability. The solution uses Q-learning, a popular RL algorithm, to train an agent to make optimal decisions for energy management.


## Features

- **Custom 5G Environment**: Simulates a 5G network using the OpenAI Gym framework with mock traffic load data.
- **Dynamic Power Modes**:
  - Normal Mode: High energy consumption, suitable for heavy traffic.
  - Power-Saving Mode: Low energy consumption, activated during low traffic.
- **Q-learning Algorithm**:
  - Implements state-action value updates for optimal decision-making.
  - Balances exploration and exploitation using an epsilon-greedy strategy.
- **Data Visualization**:
  - Generates multiple graphs to analyze energy consumption, rewards, actions, and traffic loads.

## Requirements

- Python 3.7 or above
- Libraries:
  - `numpy`
  - `gym`
  - `matplotlib`

Install required dependencies using:
```bash
pip install numpy gym matplotlib
```

## How It Works

1. **Environment Setup**:
   - Traffic loads are simulated with random values between 1 and 100.
   - States represent current network loads.
   - Actions include switching between Normal and Power-Saving Modes.

2. **Q-learning Training**:
   - The Q-table is initialized with zeros.
   - The agent learns optimal actions over multiple episodes by interacting with the environment and receiving rewards.
   - Rewards:
     - Positive for activating Power-Saving Mode during low loads.
     - Penalty for using Power-Saving Mode during high loads.
   - The trained Q-table maps states to optimal actions.

3. **Testing**:
   - The trained agent is tested on the environment to evaluate energy savings and decision-making efficiency.

4. **Visualization**:
   - Graphs analyze total energy consumption, rewards, actions taken, and network load vs. energy consumption.

## Visualizations

- **Total Energy Consumption**: Shows cumulative energy usage across steps.
- **Rewards**: Highlights rewards earned for energy-efficient decisions.
- **Actions**: Displays switching between Normal and Power-Saving Modes.
- **Network Load vs. Energy Consumption**: Correlates traffic loads with energy usage.

## Usage

Run the script to train the agent, test its performance, and generate insights:
```bash
python 5g_energy_optimization.py
```

## Results

The system demonstrates a significant reduction in energy consumption by adapting power modes to network traffic dynamically, ensuring sustainable 5G operations.

## Future Enhancements

- Incorporate real-world traffic data.
- Extend to multi-agent scenarios for large-scale networks.
- Add more operational modes for finer control of energy consumption.

## Acknowledgment

Thanks to Dr. Bhupender Kumar for his invaluable guidance and support throughout this project. His expertise and insights have been instrumental in shaping the direction and execution of this work. We deeply appreciate his encouragement and mentorship, which have greatly contributed to the success of this study.

## Team Members

- **Param Prajapati** (202111066)  
- **Prakhar Shukla** (202111067)  
- **Shivam Mohit** (202111077)  
- **Hiren Sinh** (202111079)  
- **Unik Yadav** (202111083)  
