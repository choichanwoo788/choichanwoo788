<div align="center">

# Choi Chanwoo

### Robotics SW Engineer

Mechanism · Control · ROS 2 · Vision · Simulation · LLM/VLA

I build robot software that connects real hardware, perception, control logic, simulation, and AI agents into reliable operating systems.

[![GitHub](https://img.shields.io/badge/GitHub-choichanwoo788-181717?style=for-the-badge&logo=github)](https://github.com/choichanwoo788)
[![Email](https://img.shields.io/badge/Email-chlcksdn27%40naver.com-005FF9?style=for-the-badge&logo=maildotru&logoColor=white)](mailto:chlcksdn27@naver.com)

</div>

---

## About Me

I am a robotics software engineer who understands both the physical side of robots and the software systems that make them useful in the real world.

My work focuses on building robot systems that do not only move once in a demo, but keep working when sensors, timing, operators, network load, and real hardware become imperfect.

| Area | What I Build |
| --- | --- |
| Robot Operation SW | ROS 2 control flows, state machines, GUI-linked operation, emergency stop, recovery |
| Autonomous Robots | SLAM, Nav2, AMR tracking, sensor-based navigation, multi-robot coordination |
| Vision & Perception | YOLO, OpenCV, RealSense, OAK-D, Depth, ArUco marker pose estimation |
| AI Robot Control | LLM/VLA task planning, robot code generation, prompt/runtime optimization |
| Digital Twin & RL | Isaac Sim, Isaac Lab, PPO, Pick & Place policy learning, TCP extension control |

---

## Tech Stack

| Category | Stack |
| --- | --- |
| Robotics | ![ROS2](https://img.shields.io/badge/ROS%202-22314E?style=flat-square&logo=ros&logoColor=white) ![Nav2](https://img.shields.io/badge/Nav2-44546A?style=flat-square) ![SLAM](https://img.shields.io/badge/SLAM-4B8BBE?style=flat-square) ![Doosan](https://img.shields.io/badge/Doosan%20M0609-005BAC?style=flat-square) ![TurtleBot4](https://img.shields.io/badge/TurtleBot4-2E8B57?style=flat-square) |
| AI / Vision | ![YOLO](https://img.shields.io/badge/YOLO-00FFFF?style=flat-square&logo=yolo&logoColor=black) ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square) ![Whisper](https://img.shields.io/badge/Faster--Whisper-111111?style=flat-square) |
| LLM / VLA | ![LLaMA](https://img.shields.io/badge/LLaMA-6F4CFF?style=flat-square) ![Qwen](https://img.shields.io/badge/Qwen2.5--Coder-1E88E5?style=flat-square) ![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white) |
| Simulation / Control | ![Isaac Sim](https://img.shields.io/badge/Isaac%20Sim-76B900?style=flat-square&logo=nvidia&logoColor=white) ![Isaac Lab](https://img.shields.io/badge/Isaac%20Lab-4CAF50?style=flat-square) ![MATLAB](https://img.shields.io/badge/MATLAB-E16737?style=flat-square) ![Simulink](https://img.shields.io/badge/Simulink-F2A900?style=flat-square) |
| Software | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) ![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white) ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black) |

---

## Project Map

```mermaid
flowchart LR
    A["ROS 2 Operation SW<br/>M0609 cooking automation"] --> B["AMR Navigation<br/>SLAM / Nav2 / safety guidance"]
    B --> C["VLA Robot Assistant<br/>LLM planning + robot code generation"]
    C --> D["Digital Twin & RL<br/>Isaac Sim / Isaac Lab / PPO"]

    A -. "reliability" .-> E["State-based robot systems"]
    B -. "perception" .-> E
    C -. "AI planning" .-> E
    D -. "simulation validation" .-> E
```

---

## Main Projects

| Project | Core Idea | My Main Contribution | Keywords |
| --- | --- | --- | --- |
| **ROS 2 Robot Cooking Automation** | Doosan M0609-based pork cutlet cooking automation system | Central controller, state-based operation, emergency stop, recovery flow, GUI-linked monitoring | ROS 2, M0609, Flask, React, State Machine |
| **AMR Construction Site Guidance** | AMR safety guidance system for heavy equipment environments | Vehicle tracking, distance keeping, sensor delay analysis, camera/network load tuning | TurtleBot4, Nav2, SLAM, YOLO, Depth |
| **VLA Collaborative Robot Assistant** | Natural language to robot task planning and executable M0609 code | Coder LLM design, Qwen2.5-Coder integration, prompt lightweighting, 60s to 10s response improvement | VLA, LLM, Qwen, LLaMA, WebSocket |
| **Digital Twin & RL Robot Control** | Isaac Sim-based Pick & Place with reinforcement learning | Isaac Sim Extension + TCP architecture, ArUco pose estimation, PPO Pick policy design | Isaac Sim, Isaac Lab, PPO, ArUco, TCP |

---

## Project Details

### 1. ROS 2-Based Robot Cooking Automation System

> Automated pork cutlet cooking process with Doosan M0609 and ROS 2 operation software.

```mermaid
flowchart TD
    UI["GUI<br/>Request / Stop / Recovery"] --> CTRL["Central Controller<br/>state validation"]
    CTRL --> TASK["Task Server Nodes<br/>seasoning / tenderizing / frying / saucing"]
    TASK --> ROBOT["Doosan M0609<br/>motion execution"]
    ROBOT --> LOG["Logs & Status<br/>monitoring dashboard"]
    CTRL --> SAFE["Emergency Stop<br/>direct controller stop"]
    SAFE --> REC["Recovery Flow<br/>diagnose and restart"]
```

**Highlights**

- Built a state-based command flow between GUI, controller, and robot task modules
- Prevented duplicate execution and unsafe commands through central validation
- Implemented immediate stop and recovery logic for real robot operation
- Designed a dashboard for process status, robot logs, stop, and restart

---

### 2. SLAM and Autonomous Driving AMR Guidance System

> Construction-site AMR guidance system using SLAM, Nav2, YOLO, and Depth sensing.

| Problem | Solution |
| --- | --- |
| Camera and network latency appeared during integrated tests | Lowered camera workload to 15 fps and 640p, used compressed image transport |
| Vehicle tracking became unstable under real-time load | Tuned distance-keeping parameters and control response |
| Individual module tests were not enough | Verified sensor freshness, communication load, and controller delay in integrated operation |

**Highlights**

- Built vehicle recognition and distance-keeping tracking with RGB/Depth input
- Connected perception output to ROS 2 driving control
- Worked with TurtleBot4, SLAM Toolbox, Nav2, AMCL, OAK-D/Depth camera, and LiDAR

---

### 3. VLA-Based Collaborative Robot Assistant

> Semantic AI assistant that turns natural language instructions into executable robot control logic.

```mermaid
flowchart LR
    USER["Natural Language<br/>voice/text command"] --> MACRO["Macro Planner<br/>task decomposition"]
    MACRO --> MICRO["Micro Planner<br/>safe motion sequence"]
    MICRO --> CODER["Coder LLM<br/>M0609 Python code"]
    VISION["Vision AI<br/>YOLO / RealSense"] --> MICRO
    CODER --> EXEC["ROS 2 / WebSocket<br/>approval and execution"]
    EXEC --> M0609["Doosan M0609<br/>robot action"]
    EXEC --> DB["Firebase<br/>logs and monitoring"]
```

**Highlights**

- Designed a Macro Planner, Micro Planner, and Coder LLM architecture
- Built Coder LLM flow using Qwen2.5-Coder for M0609 control logic generation
- Reduced Coder LLM response time from about **60s to 10s** through prompt lightweighting and template-based code merging
- Connected vision, gesture fallback control, Firebase logging, and robot execution

---

### 4. Digital Twin and Reinforcement Learning Robot Control

> Isaac Sim and Isaac Lab-based Pick & Place simulation with PPO policy learning.

| Component | Implementation |
| --- | --- |
| Simulation | Isaac Sim, Isaac Lab, M0609, suction gripper, RealSense-style camera |
| Perception | ArUco marker detection and camera-to-world coordinate transformation |
| Policy | PPO-based Pick policy with approach, suction, lifting, and stabilization phases |
| Runtime Architecture | Isaac Sim Extension handles Stage control, external TCP client sends commands |

**Highlights**

- Verified ArUco marker pose estimation with about **1 mm** error against ground truth
- Built relative observation values from end-effector and marker positions
- Solved Python 3.10 ROS 2 and Python 3.11 Isaac Sim context conflicts using an Extension + TCP server structure
- Separated external command transmission from internal simulation execution for stable automation

---

## Engineering Direction

```mermaid
mindmap
  root((Robotics SW))
    Reliable Operation
      State machines
      Recovery flows
      Runtime logs
    Perception-Aware Control
      Vision
      Depth
      Sensor freshness
    AI Robot Systems
      LLM planning
      Code generation
      Safety boundaries
    Simulation Validation
      Isaac Sim
      Reinforcement learning
      Digital twin
```

I want to keep building robot systems that combine reliable operation software, perception-aware control, simulation-based verification, and AI agents that can plan or generate behavior without losing safety boundaries.

---

## Contact

| Channel | Link |
| --- | --- |
| GitHub | [github.com/choichanwoo788](https://github.com/choichanwoo788) |
| Email | [chlcksdn27@naver.com](mailto:chlcksdn27@naver.com) |
