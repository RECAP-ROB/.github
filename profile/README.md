# 🤖 RECAP (Robotic Enhanced Commodity Arrangement and Placement) System

RECAP is an autonomous mobile robotic system designed to provide continuous shelf monitoring and restock shelves when goods are depleted. 

Developed to mitigate the retail challenges of "Ghost Stock," this system also protects supermarket attendants from repetitive strain injuries by automating the physically demanding restocking process.

## 🚀 Core Capabilities

*   **Continuous Shelf Monitoring:** Utilizes a custom-trained YOLOv11 model on a Raspberry Pi Camera Module 3 to detect missing items, misplaced products, and blocked shelves in real-time.
*   **Autonomous Navigation:** Employs 2D LiDAR SLAM for mapping and the ROS 2 Nav2 stack for dynamic obstacle avoidance and path planning through complex supermarket aisles.
*   **Robotic Manipulation:** Features a custom 5-DoF robotic arm with a 1-DoF gripper, guided by stereo vision depth perception and Rapidly-exploring Random Tree (RRT) motion planning, to execute precise pick-and-place operations.
*   **Inventory Intelligence:** Integrates a Django-based web platform to maintain persistent stock levels and dispatch asynchronous restock missions via a Celery task queue.

## 🛠️ Technology Stack

*   **Hardware:** Raspberry Pi 4B, Arduino Mega 2560, ESP32 cameras, RPLIDAR A1, and L298N motor drivers.
*   **Software & Middleware:** ROS 2, OpenCV, Ultralytics YOLO, Nav2, SLAM Toolbox, and PyTrees for behavior-tree state management.
*   **Web Integration:** Django REST Framework, React (TypeScript), Celery, Redis, and MQTT for high-frequency sensor telemetry.

## 📁 Repository Guide

*   **`RECAP_SRC`**: Core source code unifying the robotic subsystems.
*   **`recap_robot`**: Simulation environment and configurations.
*   **`Depth_playground`**: Depth perception and stereo vision algorithms.
*   **`Manipulator`**: Kinematics and control scripts for the 5-DoF robotic arm.
*   **`RECAP_INVENTORY`**: The React/Django web-based inventory management platform.
*   **`Models_and_URDFs`**: CAD designs and URDF files for the physical robot.

## 👥 The RECAP Team

This project was developed by a team of final-year BSc. Electronic and Computer Engineering students at Jomo Kenyatta University of Agriculture and Technology (JKUAT).

*   **Barbra Gitonga:** Robot chassis and arm design, and arm manipulation
*   **Ian Ndirangu:** Navigation and Path Planning
*   **Maria Akinyi:** Obstacle Avoidance
*   **Mohamed Ibrahim:** Object Detection for Product Replenishment
*   **Osteen Ng’etich:** Web-based Inventory Management System

### 🔧 Hardware Assembly
The team worked hands-on to integrate the Raspberry Pi, motor drivers, LiDAR, and acrylic chassis.
![Team assembling the chassis](images/20260319_143909.jpg)
![Wiring the robot](images/IMG-20260328-WA0020.jpg)
![Mounting the LiDAR](images/20260319_152547.jpg)
