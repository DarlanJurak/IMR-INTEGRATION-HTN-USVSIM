# IMR-INTEGRATION-HTN-USVSIM

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
