# IMR-INTEGRATION-HTN-USVSIM

# What is this

This project consists on an integration of an **Hierarchical Task Network (HTN) automated-planning system** and an **Unmanned Surface Vehicle (USV) simulator**. In this way its possible to simulate USVs in a realistic environment and implement autonomous guidance.

### HTN automated-planning system:  
JSHOP2  -> http://www.cs.umd.edu/projects/shop/description.html
### USV simulator:                  
USV_SIM -> https://github.com/disaster-robotics-proalertas/usv_sim_lsa


Below we can see the main architecture of this project:
![Integration_Architecture\label{Integration_Architecture}](Integration_Architecture.png)

# What it does

Currently, the system is capable to guide one USV and try to avoid possible Head-On collision situations being compliant to the COOLREGs (Convention on the International Regulations for Preventing Collisions at Sea, 1972). The USV_GUIDER block is implemented in python and must be edited to allow new features.

# How to compile

Experiment Replication - General Instructions:
For replication of the presented experiment 3 main repository are required: JSHOP2 fork, USV SIM, and USV GUIDER. It is required to install the USV SIM epository as a catkin package and run the repository as follow:

    ~/catkin_ws$ \atkin_make_isolated --install
    ~/catkin_ws$ source install_isolated/setup.bash
    ~/catkin_ws$ roslaunch usv_sim airboat_scenario4_intruder.launch parse:=true
    ~/catkin_ws$ roslaunch usv_sim airboat_scenario4_intruder.launch parse:=false gui:=true
    
After simulation is opened its necessary to click start in the gazebo simulator.
For the USV_GUIDER execution is required to run:

    /USV_GuidanceSystem$ ./run.sh

Is expected that after the execution of the command above, the controlled boat start to move straight ahead.


# How to execute a example
