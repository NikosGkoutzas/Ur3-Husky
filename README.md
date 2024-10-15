# Ur3-Husky
<h1><b><I>My Master's Thesis:</I> Analysis and Simulation of a 6 DOP Robotic Arm on a Wheeled Vehicle with Application in Object Sorting</b></h1>
<b>Introduction</b>

This thesis focuses on the collaboration between two robots, the Husky UGV and the UR3 robotic arm, to autonomously recognize, collect, and place objects based on their color. The mission involves navigating through the environment, identifying objects on various tables, grasping them with the UR3, and placing them into designated holes on different tables.
Objective

The goal of this work is to develop an autonomous system that allows the two robots to work harmoniously together to recognize, collect, and place objects in predetermined locations based on color recognition. The Husky is responsible for navigation and locating the tables, while the UR3 executes the precise grasping and placement of the objects.
System Description
<b><br>1. Husky Robot</b>

The Husky UGV is a four-wheeled robotic vehicle equipped with a camera that enables it to navigate autonomously through the environment. The camera helps avoid collisions with objects and ensures accurate approaches to the tables.
Husky Functionalities:

    Utilizing its camera for navigation and obstacle avoidance.
    Detecting the locations of tables with objects and those with holes.
    Sending position and type data to the UR3 for object grasping.

<b>2. UR3 Robot</b>

The UR3 is a six-axis robotic arm equipped with two cameras and a gripper. The first camera is used for recognizing and grasping objects from the tables, while the second camera is mounted vertically on the arm and looks down at the ground for accurate placement of the objects into the holes.
UR3 Functionalities:

    Camera 1: Used for horizontal grasping of objects based on their color.
    Camera 2: Looks vertically at the ground and enables precise placement of objects into corresponding holes.
    Accurate handling of objects using the UR3 gripper and collaboration with the Husky for transporting them.

<b>Kinematic and Inverse Kinematic Calculations</b>

All kinematic and inverse kinematic equations for the UR3 robotic arm have been calculated and integrated into the code to ensure the accuracy of the arm's movements during grasping and placement actions. The implementation was carried out in Python using ROS Noetic and the Gazebo simulator.

    Kinematic Analysis: Calculates the precise position and orientation of the UR3 concerning the arm's joints.
    Inverse Kinematics: Computes the necessary angles to achieve the desired position of the arm's end effector (gripper).

<b>Navigation and Grasping Control Algorithms</b>

All algorithms for navigating the Husky to the tables, accurately positioning it at the center of the tables, as well as the procedures for grasping and placing the objects from/to the tables, were designed and fully implemented by me. These algorithms allow:

    Accurate Navigation: The Husky dynamically corrects its path to reach the center of the table precisely.
    Smooth Execution: The UR3 performs grasping and placement actions with high precision based on camera data and kinematic equations.

<b>Robot Collaboration</b>

The collaboration process includes the following steps:

    Object Recognition: The UR3 uses its first camera to identify and categorize the objects on the tables based on color.
    Navigation and Collection: The Husky navigates using its camera to approach the tables, where the UR3 then grasps the objects.
    Object Placement: The Husky moves to a table with holes, and the UR3 uses its second camera to accurately place the objects into the holes based on their color.
    Process Repetition: The procedure continues until all objects are placed in their respective locations.

<b>Operating Modes</b>

At the start of the system, two operating modes are offered:

    Auto Mode: In this mode, the robots operate collaboratively and autonomously perform the mission from object recognition to placement.
    Manual Mode: In this mode, the user can individually control the operation of the robots, whether for the Husky's navigation or the UR3's movements. This allows for testing specific functionalities and debugging the system.

<b>Technologies and Tools</b>

    ROS Noetic: Used for coordinating the two robots and enabling communication between them.
    Gazebo: A simulator used for realistically representing the movements of the Husky and UR3.
    OpenCV: For recognizing and categorizing objects based on color through images from the cameras.
    UR3 Driver: Used for controlling the movement of the UR3 robotic arm.
    Python: Used to implement the kinematic and inverse kinematic equations of the arm.

<b>Challenges and Solutions</b>

    Accurate Color Recognition: The detection of object colors can be affected by changes in lighting. To address this issue, color filters and camera brightness adjustments were implemented.
    Robot Synchronization: Achieving precise synchronization of movements between the Husky and UR3 requires accurate communication. This was achieved through ROS and properly programmed movement scenarios.

<b>Conclusions</b>

This thesis presents a comprehensive solution for collaboration between two robots to recognize and place objects based on their color. The successful implementation demonstrates the capability for coordinated action between two autonomous systems, providing a platform that can be applied in industrial applications such as object sorting and robotic assembly.

<b>Installation Instructions</b>

    Clone the repository:
        git clone https://github.com/QualiaT/husky_ur3_simulator in order to install all the necessary packages for ur3, husky robots, sensors and cameras.
