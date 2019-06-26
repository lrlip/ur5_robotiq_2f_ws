# ur5_robotiq_2f_ws
Working Gazebo simulation of UR5 with Robotiq 2-finger gripper controlled with MoveIt!. 

This repository contains the packages ur5 and robotiq downloaded from https://github.com/utecrobotics/ur5.
The robotiq_ur5 package contains the MoveIt setup to control the Gazebo simulation with MoveIt.

## Installation
Go to your workspace/src
```bash
git clone https://github.com/lrlip/ur5_robotiq_2f_ws.git
cd ..
catkin_make
source devel/setup.bash
```
Instal the ros controllers
```bash
sudo apt-get install ros*controller*
```

## Starting Gazebo Simulation

The simulation is launched by:
```bash
$ roslaunch ur5_gazebo ur5_cubes.launch
```
or 
```bash
$ roslaunch ur5_gazebo ur5_setup.launch
```

The simulation starts paused. Unpause to use the simulation by MoveIt.

## Starting MoveIt control

Launch the MoveIt control by:
```bash
$ roslaunch robotiq_ur5 robotiq_ur5_planning_execution.launch
```
You now should see the same posture in the Gazebo as the MoveIt environment.
Set in Rviz the `MotionPlanning/Planning Request/Planning Group` to manipulator to drag the arm around. 
By `Plan and Execute` the arm will move to its new position.
