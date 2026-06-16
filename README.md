# Choi Chanwoo

Robotics SW Engineer focused on ROS 2, robot control, perception, simulation, and AI-assisted robot systems.

I build robot software with an engineering view that connects mechanism, dynamics, control, sensing, and runtime reliability. My projects mainly explore how real robots can move safely and consistently in changing environments, from ROS 2-based operation software to VLA/LLM robot control and Isaac Sim reinforcement learning.

[![GitHub](https://img.shields.io/badge/GitHub-choichanwoo788-181717?style=flat-square&logo=github)](https://github.com/choichanwoo788)
[![Email](https://img.shields.io/badge/Email-chlcksdn27%40naver.com-005FF9?style=flat-square&logo=maildotru)](mailto:chlcksdn27@naver.com)

## Focus

- Robot software architecture with ROS 2, state machines, service/action nodes, and real robot operation flows
- Cobot and AMR control with Doosan M0609, TurtleBot4, Nav2, SLAM, and sensor-driven behavior
- Vision-based robot perception using OpenCV, YOLO, RealSense, OAK-D, Depth, and ArUco markers
- LLM/VLA-based robot task planning, code generation, and prompt/runtime optimization
- Digital twin and reinforcement learning with Isaac Sim, Isaac Lab, PPO, and TCP-based extension control

## Tech Stack

**Robotics**
ROS 2, Nav2, SLAM Toolbox, AMCL, DDS, Doosan M0609, TurtleBot4, RealSense, OAK-D Pro, RPLiDAR

**AI / Vision**
YOLO, OpenCV, MediaPipe, Faster-Whisper, LLaMA, Qwen2.5-Coder, Ollama, PyTorch, 1D-CNN, LSTM, PPO

**Simulation / Control**
Isaac Sim, Isaac Lab, MATLAB, Simulink, RecurDyn, robot kinematics, compliance control, force control

**Software**
Python, C/C++, Linux, Git, Flask, React, SQLite, Firebase, WebSocket, Modbus TCP

## Main Projects

### ROS 2-Based Robot Cooking Automation System

Built a robot operation system for an automated pork cutlet cooking process using a Doosan M0609 cobot.

- Designed a central controller structure that validates GUI requests before passing commands to robot task modules
- Improved the operation flow from direct GUI execution to state-based command handling
- Implemented emergency stop and recovery logic so the robot can stop immediately, diagnose its state, and return to a restartable condition
- Built a GUI environment for process requests, robot status monitoring, logs, stop, and recovery

**Keywords:** ROS 2, Doosan M0609, Flask, React, state machine, emergency stop, recovery, robot operation software

### SLAM and Autonomous Driving AMR Guidance System

Developed an AMR-based safety guidance system for construction sites where heavy equipment and workers share the same workspace.

- Used TurtleBot4, SLAM, Nav2, LiDAR, and camera-based perception for site navigation and guidance
- Implemented vehicle recognition and distance-keeping tracking using RGB/Depth data
- Tuned tracking parameters, camera frame rate, resolution, and compressed image transport to reduce delay and communication load
- Learned the importance of verifying sensor latency, network load, and control response in integrated robot systems

**Keywords:** ROS 2, TurtleBot4, Nav2, SLAM, AMCL, YOLO, Depth camera, multi-robot operation

### VLA-Based Collaborative Robot Assistant

Built a semantic AI robot assistant that converts natural language commands into executable robot control code.

- Designed a three-stage architecture: Macro Planner, Micro Planner, and Coder LLM
- Built the Coder LLM flow using Qwen2.5-Coder to generate M0609 Python control logic
- Reduced Coder LLM response time from about 60 seconds to about 10 seconds by lightweighting prompts and generating only core control logic
- Connected vision, gesture backup control, WebSocket communication, Firebase logging, and robot execution into one runtime flow

**Keywords:** VLA, LLM, Qwen2.5-Coder, LLaMA, ROS 2, Doosan M0609, WebSocket, Firebase, RealSense, YOLO

### Digital Twin and Reinforcement Learning Robot Control

Built a simulation-based Pick & Place control structure using Isaac Sim, Isaac Lab, and reinforcement learning.

- Created an Isaac Sim and Isaac Lab environment for M0609, suction gripper, RealSense, and ArUco-marker-based box tracking
- Used ArUco and depth data to transform camera coordinates into world coordinates and generate relative observations for policy learning
- Verified marker pose estimation with about 1 mm position error against ground truth in the simulation setup
- Designed PPO-based Pick policy learning with approach, suction, lifting, and stabilization phases
- Solved Isaac Sim Python context and ROS 2 Python version conflicts by moving Stage control into an Isaac Sim Extension and sending external commands through a TCP client/server structure

**Keywords:** Isaac Sim, Isaac Lab, PPO, reinforcement learning, ArUco, TCP server, extension, digital twin, Pick & Place

## What I Care About

I like robot software that does not only move once in a demo, but keeps working when timing, sensors, operators, and real hardware become imperfect.

My current direction is to build robot systems that combine:

- reliable operation software,
- perception-aware control,
- simulation-based verification,
- and AI agents that can plan or generate robot behavior without losing safety boundaries.

## Contact

- GitHub: [github.com/choichanwoo788](https://github.com/choichanwoo788)
- Email: [chlcksdn27@naver.com](mailto:chlcksdn27@naver.com)
