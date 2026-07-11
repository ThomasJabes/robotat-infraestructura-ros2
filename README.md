# Infrastructure for Robotic Swarm Control with ROS2 and MOCAP4ROS2

This repository is part of the graduation project **"Implementation of infrastructure for robotic swarm control with ROS2 and motion capture within the Robotat ecosystem"**, developed at **Universidad del Valle de Guatemala**.

The goal of the project is to establish a distributed infrastructure based on **ROS2**, integrating the **MOCAP4ROS2** package with the **OptiTrack** motion capture system, and using **CrazySwarm2** and **MQTT** for coordination and communication between robotic agents.

---

## General Architecture

<p align="center">
  <img width="900" alt="Robotat ROS2 Infrastructure" src="https://github.com/user-attachments/assets/a7b8895a-c5bb-45e9-bc59-fdf6f8b8cc8e" />
</p>

1. **Motion capture:** OptiTrack system managed by Motive.
2. **Data transmission:** Via the **NatNet** and **MQTT** protocols.
3. **Processing:** On a **ROS2** server running the **MOCAP4ROS2** package inside a Docker container.
4. **Experimental validation:** With multiple **Pololu 3pi+** robots synchronized in real time.

---

## Current workspace

This repository currently includes the **MQTT communication** environment, responsible for message exchange between the motion capture system and the ROS2 server.

The remaining components — Docker images, ROS2 nodes, and technical documentation — are available at the following link:

🔗 **[General project repository (Google Drive)](https://drive.google.com/drive/folders/1ajJXgjBkqGwcT6tUxGNX3f0VVaDPKLEW?usp=sharing)**

Summary video: https://youtu.be/ge7PwUTfvk8

---

## Main technologies

- **ROS2 Humble**
- **MOCAP4ROS2**
- **CrazySwarm2**
- **Docker**
- **OptiTrack + Motive**
- **MQTT (Eclipse Mosquitto)**

---

## Basic Docker commands

```bash
# Check available images
docker images

# Load exported .tar image
sudo docker load -i crazyflie_ros2_humble.tar

# Run the container
sudo docker run -it crazyflie-ros2:humble

# Rebuild image if there are changes
sudo docker build -t crazyflie-ros2:humble .
```
