# robotic-arm-kinematics-path-planning
Robotic Arm Kinematics & Path Planning

Project 1 — DecodeLabs Robotics & Automation Internship (Batch 2026)

A simulated 6-axis robotic arm that moves accurately from a start pose to a target pose without colliding with obstacles, using Inverse Kinematics for joint-angle calculation and a collision-aware motion-planning pipeline.

📌 Overview

This project demonstrates the core computational pipeline behind robotic motion planning:

Forward Kinematics — deriving end-effector position from known joint angles
Inverse Kinematics (IK) — calculating required joint angles for a target XYZ pose
Collision-aware trajectory planning — generating a smooth path that avoids obstacles
Simulated execution — validating the full pipeline in RViz2 / MoveIt2
🛠️ Tools & Stack
Component	Tool
OS / Environment	Windows 10 + WSL2 (Ubuntu 22.04 LTS)
Middleware	ROS2 Humble
Visualization	RViz2
Motion Planning	MoveIt2 (OMPL / RRTConnect)
Collision Checking	FCL (Flexible Collision Library)
Robot Models	Universal Robots UR5 (Forward Kinematics demo), Franka Panda (IK + planning demo)
Build System	colcon
⚙️ What Was Done
Set up a complete ROS2 + MoveIt2 development environment from scratch on WSL2.
Loaded a UR5 6-axis arm URDF into RViz2 and manually verified Forward Kinematics using joint sliders.
Used MoveIt2's Motion Planning interface with a Franka Panda arm to demonstrate Inverse Kinematics — dragging an interactive marker to a target pose and letting the solver compute joint angles.
Added an obstacle (box) to the planning scene and verified that MoveIt2's collision-aware planner (OMPL + FCL) generated a path that avoided it.
Successfully planned and executed multiple collision-free trajectories, confirmed visually in RViz2.
📷 Results

See /screenshots for RViz2 captures showing:

The obstacle placed in the planning scene
The interactive IK marker set on the target pose
The successfully executed, collision-free trajectory

Full write-up, methodology, and challenges/solutions are documented in Project1_Report.docx.

⚠️ Scope Note

Gazebo physics simulation (gravity, contact dynamics, PID-tuned execution) was scoped out of this milestone due to the one-week timeframe and is proposed as a future extension. All kinematics, IK solving, and collision-aware planning were fully demonstrated and verified in RViz2/MoveIt2.

🚀 Next Steps

This environment and workspace carry forward into the remaining weeks of the DecodeLabs Robotics & Automation internship.

Author: Ali Hassan BS Artificial Intelligence, Emerson University Multan
