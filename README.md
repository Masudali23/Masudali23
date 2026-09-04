<p align="center">
  <img src="https://raw.githubusercontent.com/Masudali23/Masudali23/main/Banner.jpg" alt="Masud Ali" width="100%" />
</p>
<h1 align="center">Hi, I'm Masud Ali 👋</h1>
 
<h3 align="center">
  B.Tech Electrical Engineering · IIT (BHU) Varanasi<br>
  Fault-tolerant control · Aerial–ground autonomy · Multi-agent reinforcement learning
</h3>
<p align="center">
  <a href="https://linkedin.com/in/masud-ali-637722298"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:masud.ali.cd.eee23@itbhu.ac.in"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <a href="https://kaggle.com/masudali07"><img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" alt="Kaggle"/></a>
  <img src="https://komarev.com/ghpvc/?username=masudali23&label=Profile%20views&color=0e75b6&style=for-the-badge" alt="views" />
</p>
---
 
I build autonomous systems and try to be honest about where they break.
 
Most of my work sits where control theory meets a vehicle that can actually fail — a
quadrotor that loses a rotor mid-mission, a ground vehicle with no navigation sensors
at all, a factory line where a silent addressing bug surfaces months later as an
intermittent fault. I care less about the demo that works and more about the boundary
where it stops working, and about being able to measure that boundary.
 
Off the keyboard I run robotics at IIT (BHU) Varanasi — Joint Secretary of the
Robotics Club, now Senior Advisor, leading a 70-member team and running competitions
for 700+ students a season.
 
---
 
## 🔬 Research
 
**Quadrotor Flight Through One and Two Rotor Failures** · `PX4` `INDI` `CUSUM` `Gazebo`
A fault-tolerant stack implemented entirely inside PX4 firmware. Detects complete rotor
loss from **inertial measurements alone** — no ESC telemetry — isolating the failed rotor
in **44–48 ms with zero false alarms** across aggressive healthy flight, then continues the
mission: position hold at σ = 0.30 m, under 2 m cross-track error after a failure at
4.7 m/s, landing within 0.9 m of home. Extends to **simultaneous double failures**, with a
set-valued isolation test, a two-survivor cascade law, and a continuous sink-rate servo
that lands below 2 m/s, upright and self-disarmed.
*Sole author, technical report.*
 
**Aerial Depth Mapping for a Ground Vehicle With No Navigation Sensors** · `RGB-D` `2.5-D mapping` `frontier exploration`
A car with no GNSS, IMU, wheel odometry, lidar or camera — its **entire navigation stack
is one downward-looking RGB-D camera on a quadrotor**. A two-sided corridor test cut
falsely-labelled road area from **35.8% → 11.1%**; ribbon-constrained frontier exploration
raised surveyed road length from **244 m → 537 m** on a 775 m course; and a measured
detection window (validity 0.93 at 2.5–3.5 m separation, collapsing to 0.02 by 5.5 m)
explained a class of permanent mission stalls.
*Sole author, technical report.*
 
**Automated GX Works3 Ladder-Logic Generation for Mitsubishi PLCs** · `Flask` `Python` `industrial automation`
A web tool generating complete, importable ladder programs and device documentation for
FX5U and MELSEC iQ-R controllers. An `AddressManager` makes address conflicts impossible
by construction; a `StepCounter` reproduces GX Works3 instruction step costs exactly.
**~60 h → ~6 h per machine (≈90%)**, guarded by 214 automated tests.
*Sole author, technical report · built during the Bajaj Auto internship.*
 
**UAV-Assisted Federated Learning & Multi-Agent RL** · `MAPPO` `federated learning` `Byzantine robustness`
Research contributor, Dept. of Electronics Engineering, IIT (BHU) — advisor Prof. Om Jee
Pandey. A MAPPO control plane where one agent per UAV jointly decides the training cohort
and next hover position, plus the poisoning attack/defence evaluation across the hierarchy.
*Ongoing.*
 
---
 
## 🤖 Robotics & Autonomy
 
| Project | Description |
|---|---|
| **Autonomous Warehouse Inventory System** <br> *Inter IIT Tech Meet 14.0 — 4th of 23 IITs* | Holonomic mecanum robot with a 2 m vertical scanning column. 2D pose-graph SLAM on an optimised Open Karto backend with EKF fusion (wheel odometry + IMU); custom YOLOv8n hitting 90%+ detection on 5×5 cm QR codes. `ROS 2` `Nav2` `SLAM` `YOLOv8` |
| **Quadrotor Single-Motor-Failure Recovery** <br> *Inter IIT Tech Meet 13.0 — ideaForge* | Stable hover and controlled landing after complete failure of one motor, reallocating control authority across the remaining three rotors with EKF attitude estimation under asymmetric thrust. `PX4` `MAVROS` `EKF` |
| [**PX4 Iris Drone Path Planning + CV**](https://github.com/Masudali23/PX4-Iris-Drone-Path-Planning-CV) | Iris PX4 drone in ROS 2 / MAVROS for real-time obstacle avoidance and autonomous field survey, with YOLO-based weed detection and image segmentation. `ROS 2` `MAVROS` `YOLO` |
| [**EKF Tracking of a Ground Bot**](https://github.com/Masudali23/EKF_Tracking_Of_Ground_Bot) | Extended Kalman Filter fusing noisy Lidar + Radar to estimate position and velocity, evaluated against ground truth. `Python` `sensor fusion` |
| **Logistics Co-Bots in a Smart Warehouse** <br> *e-Yantra Robotics Competition 2024–25, IIT Bombay* | Dual-cobot pick-and-place with real-time vision-based package identification and an adaptive multi-agent navigation layer for shared workspaces. `ROS 2` `Nav2` `OpenCV` |
| **Robotic Basketball System** <br> *Team Lead, Robocon 2025 — National Finale* | Base design and CAD for a two-robot pneumatic shooting system; basket-detection and trajectory-optimisation pipeline; multi-robot coordination over real-time inter-robot comms. `CV` `Fusion 360` |
| [**Agricultural Manual + Autonomous Bot**](https://github.com/Masudali23/Robocon-2024) <br> *Team Robocon 2024* | Autonomous and manual bots for agricultural tasks — 2D LIDAR, IMU and YOLO for detection and navigation, with custom control strategies. `ROS` `CV` |
| **PID Temperature Controller** <br> *Exploratory Project, Dr. Shyam Kamal* | Closed-loop Arduino Nano controller with MAX6675 thermocouple and MOSFET drive, tuned by modified Ziegler–Nichols to ±0.5 °C at 47 °C within 120 s. `Embedded C` `control` |
 
---
 
## 🧠 AI & Machine Learning
 
| Project | Description |
|---|---|
| [**Multimodal Transformer 3D Object Detection**](https://github.com/Masudali23/Multimodal-Transformer-Object-Detection) <br> *Changwon National University, South Korea* | Camera + radar/LiDAR fusion via Vision Transformers, EfficientDet and 3D CNNs with TransCAR-style association; Slave/Master transformer blocks with an adaptive cross-attention controller. Benchmarked on nuScenes, Lyft Level 5 and KITTI. `PyTorch` |
| **OCR & Freshness Classification** <br> *Flipkart GRID — CV Challenge* | Deep-learning OCR for text classification and feature extraction, plus freshness assessment of fruit and vegetables. `TensorFlow` `OpenCV` |
| [**Multiple Object Detection — YOLO**](https://github.com/Masudali23/Multiple-Object-Detection-YOLO) | YOLOv3 object detection over video and webcam streams. `Python` `OpenCV` |
 
---
 
## 💼 Experience
 
**Automation Software Intern** — Bajaj Auto Ltd., Machine & Automation Technology · *May – Jul 2026*
Built the PLC ladder-logic generation tool above; designed the `AddressManager` that
eliminates silent M/D/R/T/X/Y address-conflict faults by construction.
 
**Robotics Engineer Intern (Perception & Navigation)** — Drobot Inc. · *Mar 2025 – Mar 2026*
Multi-Livox LiDAR fusion pipeline in ROS 2 with unified TF2 frame management; RANSAC
ground-plane segmentation with cliff and ramp detection; dual-mode actuator controller
at ±1 mm repeatability.
 
**Remote Research Intern** — Changwon National University, South Korea · *Dec 2024 – Feb 2025*
Multi-modal 3D object detection for autonomous driving under Prof. Oh-Seol Kwon.
 
---
 
## 🏆 Achievements
 
- **4th of 23 IITs** — Inter IIT Tech Meet 14.0 (*Eternal*), part of IIT BHU's first-ever Overall 4th-place finish
- **8th overall** — Inter IIT Tech Meet 13.0, IIT Bombay (*ideaForge*)
- **Team Robocon 2025** — led through Stages 1 and 2 to the National Finale
- **Special Mention** (top 5 of ~800) in both La Robo Liga and MAZEX — later returned as their mentor and organiser
- **Global Remote Research Internship**, Changwon National University, South Korea
---
 
## 👥 Leadership
 
- **Senior Advisor** (2026–) and **Joint Secretary** (2025–26), Robotics Club, IIT (BHU) Varanasi — 70-member team, annual hardware budget, full competition calendar for 700–800 participants a season
- **Event Head**, Kashiyatra '26 — 8 events, 1,500–2,000 participants, 150+ organising team
- **Event Manager & Robotics Category Head**, Technex '26 — Robowars, Micromouse, MAZEX, Botstacle
- **Induction Mentor**, Student Counselling Services (SAKHA) — 100+ first-years
---
 
## 🛠️ Languages and Tools
 
<p align="left">
<a href="https://www.python.org" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/></a>
<a href="https://www.w3schools.com/cpp/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="cplusplus" width="40" height="40"/></a>
<a href="https://www.cprogramming.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="c" width="40" height="40"/></a>
<a href="https://www.ros.org/" target="_blank" rel="noreferrer"><img src="https://www.vectorlogo.zone/logos/ros/ros-icon.svg" alt="ros" width="40" height="40"/></a>
<a href="https://pytorch.org/" target="_blank" rel="noreferrer"><img src="https://www.vectorlogo.zone/logos/pytorch/pytorch-icon.svg" alt="pytorch" width="40" height="40"/></a>
<a href="https://www.tensorflow.org" target="_blank" rel="noreferrer"><img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" width="40" height="40"/></a>
<a href="https://opencv.org/" target="_blank" rel="noreferrer"><img src="https://www.vectorlogo.zone/logos/opencv/opencv-icon.svg" alt="opencv" width="40" height="40"/></a>
<a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/></a>
<a href="https://numpy.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/numpy/numpy-original.svg" alt="numpy" width="40" height="40"/></a>
<a href="https://www.mathworks.com/" target="_blank" rel="noreferrer"><img src="https://upload.wikimedia.org/wikipedia/commons/2/21/Matlab_Logo.png" alt="matlab" width="40" height="40"/></a>
<a href="https://www.linux.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/></a>
<a href="https://git-scm.com/" target="_blank" rel="noreferrer"><img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/></a>
<a href="https://flask.palletsprojects.com/" target="_blank" rel="noreferrer"><img src="https://www.vectorlogo.zone/logos/pocoo_flask/pocoo_flask-icon.svg" alt="flask" width="40" height="40"/></a>
<a href="https://www.arduino.cc/" target="_blank" rel="noreferrer"><img src="https://cdn.worldvectorlogo.com/logos/arduino-1.svg" alt="arduino" width="40" height="40"/></a>
<a href="https://www.docker.com/" target="_blank" rel="noreferrer"><img src="https://www.vectorlogo.zone/logos/docker/docker-official.svg" alt="docker" width="40" height="40"/></a>
</p>
---
 
## 📊 GitHub Stats
 
<p align="center">
  <img width="48%" src="https://github-readme-stats.vercel.app/api?username=masudali23&show_icons=true&locale=en&theme=default" alt="stats" />
  <img width="41%" src="https://github-readme-stats.vercel.app/api/top-langs?username=masudali23&show_icons=true&locale=en&layout=compact&theme=default" alt="top langs" />
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com/?user=masudali23" alt="streak" />
</p>
---
 
## 📫 Reach me
 
**Email** · masud.ali.cd.eee23@itbhu.ac.in · alimasud2023@gmail.com
**LinkedIn** · [masud-ali-637722298](https://www.linkedin.com/in/masud-ali-637722298)
**Kaggle** · [masudali07](https://kaggle.com/masudali07)
 
I'm looking for collaborators and for a master's position in robotics and AI. If you
work on fault-tolerant control, aerial–ground autonomy or multi-agent RL, get in touch.
