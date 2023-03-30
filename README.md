# SmartBuildings_COVIDControl
 
In this project, we developed a data-driven controller, via an RL approach to contain the spread of airborne pathogens, specifically COVID-19, in built environments.  There are two major control problems here:

I. Airflow control: 

In the first set-up we control the airflow in a room such that the infection risk (performance measure of the control problem) is minimized. The infection risk is defined as the concentration integral over a given time period and a given spatial region of interest. For the sake of practicality, we constrain the problem to a family class of airflows known as double-vortex. The RL-based controller learns the parameters of this airflow.

II.  Disinfectant placement control:

In the second set-up, we minimize the same infection risk as in the first set-up but using disinfectants, in particular Hydrogen-Peroxide (HP). The RL-based controller learns the position of the HP source. In this set-up we assume a fixed uniform airflow in the room.


For both set-ups, physics of the problem (governed by the advection-diffusion equations) are modeled by the finite-element-based Python library, FEniCs. Our RL controller is based on the SOTA PPO algorithm (Stable Baselines3 implementation).

There are 2 main Jupyter Notebook files:

1)	SmartBuildings_COVIDControl_Main.ipynb: This is the main file to run

2)	Environment.ipynb: This is the class file that contains our developed environment classes for the building physics.

Reference:

•	Hosseinloo A. H. et al. “Data-driven control of COVID-19 spread in buildings: a reinforcement-learning approach”. IEEE Transactions on Automation Science and Engineering [under review] (2022): https://arxiv.org/pdf/2212.13559.pdf
