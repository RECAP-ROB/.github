# About RECAP 

RECAP (Robotic Enhanced Commodity Arrangement and Placement) is an autonomous mobile robotic system designed to provide continuous shelf monitoring and restock shelves when goods are depleted. 

<img width="1280" height="960" alt="IMG-20260605-WA0052" src="https://github.com/user-attachments/assets/397e485c-3c36-4bc5-a69a-76d007a41962" />

Developed to mitigate the retail challenges of "Ghost Stock," this system also protects supermarket attendants from repetitive strain injuries by automating the physically demanding restocking process.

## What RECAP does

*   **Continuous Shelf Monitoring:** Utilizes a custom-trained YOLOv11 model on a Raspberry Pi Camera Module 3 to detect missing items, misplaced products, and blocked shelves in real-time.
*   **Inventory Intelligence:** Integrates a Django-based web platform to maintain persistent stock levels and dispatch asynchronous restock missions via a Celery task queue.


https://github.com/user-attachments/assets/c00c69bf-820b-4946-8656-77e0895748d4


*   **Autonomous Navigation:** Employs 2D LiDAR SLAM for mapping and the ROS 2 Nav2 stack for dynamic obstacle avoidance and path planning through complex supermarket aisles.


https://github.com/user-attachments/assets/b7d5b139-8e0b-4a7f-baf4-2f1a5fe9b7bd


*   **Robotic Manipulation:** Features a custom 5-DoF robotic arm with a 1-DoF gripper, guided by stereo vision depth perception and Rapidly-exploring Random Tree (RRT) motion planning, to execute precise pick-and-place operations.

  
https://github.com/user-attachments/assets/d944de70-6a70-4560-8880-2dd203d3525c


## Tech used

*   **Hardware:** Raspberry Pi 4B, Arduino Mega 2560, ESP32 cameras, RPLIDAR A1, and L298N motor drivers.
*   **Software & Middleware:** ROS 2, OpenCV, Ultralytics YOLO, Nav2, SLAM Toolbox, and PyTrees for behavior-tree state management.
*   **Web Integration:** Django REST Framework, React (TypeScript), Celery, Redis, and MQTT for high-frequency sensor telemetry.

### 🏁 Game Field Layout

To validate our system in a physical space, we constructed a 4m x 3m testing environment, otherwise known as the game field.

<img width="4624" height="3468" alt="20260608_134532" src="https://github.com/user-attachments/assets/39f17a90-0004-4429-bbde-d766479307f3" />

*   **Red Arrow:** The continuous shelf monitoring system, housing the Raspberry Pi 4 and Pi Camera for real-time image processing and inventory evaluation.
*   **Green Arrow:** The custom retail shelf prototype where items are monitored and restocked.
*   **Blue Arrow:** The robot's resting place (home base) where it idles and awaits dispatch instructions from the web server.
*   **Orange Arrow:** The store area where the robot navigates to fetch new items for restocking operations.

<img width="4624" height="3468" alt="20260608_134715" src="https://github.com/user-attachments/assets/500ec50c-5bb9-40e6-b5db-8dc6c0799991" />


## A guide through this repo

*   **`RECAP_SRC`**: Core source code unifying the robotic subsystems.
*   **`recap_robot`**: Simulation environment and configurations.
*   **`Depth_playground`**: Depth perception and stereo vision algorithms.
*   **`Manipulator`**: Kinematics and control scripts for the 5-DoF robotic arm.
*   **`RECAP_INVENTORY`**: The React/Django web-based inventory management platform.
*   **`Models_and_URDFs`**: CAD designs and URDF files for the physical robot.

## The RECAP Team

This project was developed by a team of final-year BSc. Electronic and Computer Engineering students at Jomo Kenyatta University of Agriculture and Technology (JKUAT).

<img width="4080" height="3060" alt="IMG-20260605-WA0038" src="https://github.com/user-attachments/assets/1157dd7f-a890-4f81-a598-7987dc3cda42" />

<img width="960" height="1280" alt="IMG-20260605-WA0101" src="https://github.com/user-attachments/assets/6170282c-694c-4625-bd8a-720ae3225841" />

<img width="3060" height="4080" alt="IMG-20260605-WA0114" src="https://github.com/user-attachments/assets/15dc5a24-5468-4628-af50-5792e2a154b2" />

*   **Barbra Gitonga:** Robot chassis and arm design, and arm manipulation
*   **Ian Ndirangu:** Navigation and Path Planning
*   **Maria Akinyi:** Obstacle Avoidance
*   **Mohamed Ibrahim:** Object Detection for Product Replenishment
*   **Osteen Ng’etich:** Web-based Inventory Management System
