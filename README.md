
# NUCE_Sheield
# 🤖 Intelligent AI Robotic System

> An intelligent robotic system combining **Artificial Intelligence, Computer Vision, Autonomous Object Detection, Robotic Arms, Embedded Systems, Security, Sensors, and Remote Control** into one integrated platform.

---

## 📌 Project Overview

This project is an advanced intelligent robotic system designed to combine **AI-based object detection, robotic manipulation, embedded control, environmental sensing, system security, and multiple control methods** into a single integrated robotic platform.

The system uses **YOLO 11** for real-time computer vision and object detection, in addition to a **custom AI model developed specifically for the project** to detect and recognize required objects.

The detected objects can be processed by the robotic system and used to control two robotic arms capable of performing different manipulation tasks.

The complete system was designed and developed as an integrated hardware and software solution, including:

* 🤖 Two robotic arms
* 🧠 AI object detection
* 👁️ YOLO 11 computer vision
* 🎯 Custom-trained AI detection model
* 🎮 Multi-method robot control
* 🔐 RFID-based security system
* 🌡️ Environmental monitoring
* 🔥 Flame detection
* 🫧 Gas detection
* ⚡ Dual power-supply monitoring
* 🔧 Custom PCB design
* 🧩 Arduino-based embedded control
* 💻 Dedicated control application

---

# 🎯 Project Objectives

The main objectives of the project are:

1. Develop an intelligent robotic platform capable of detecting objects using AI.
2. Integrate **YOLO 11** into the robotic workflow.
3. Develop and train a custom AI model for project-specific object detection.
4. Control two robotic arms using a centralized embedded control system.
5. Provide multiple methods for controlling the robotic system.
6. Implement a security system using RFID authentication.
7. Monitor environmental conditions using multiple sensors.
8. Monitor the power system and measure the average output voltage of the two power supplies.
9. Design and develop custom PCBs for the electronic system.
10. Build a complete hardware/software architecture rather than using isolated modules.

---

# 🧠 Artificial Intelligence & Computer Vision

## YOLO 11

The project uses **YOLO 11** as one of the main computer-vision technologies.

YOLO (You Only Look Once) enables real-time object detection by processing camera frames and identifying objects directly from the captured image.

The detected objects can be used as input for the robotic system to determine the required robotic action.

### AI Pipeline

```text
Camera
   ↓
Image Acquisition
   ↓
YOLO 11
   ↓
Object Detection
   ↓
Object Classification
   ↓
Decision / Control Logic
   ↓
Robotic Arm
   ↓
Manipulation / Action
```

---

# 🤖 Custom AI Model

In addition to YOLO 11, a **custom AI model was developed specifically for this project**.

The custom model is designed to detect the objects required by the robotic application.

The model-development workflow includes:

```text
Data Collection
      ↓
Dataset Preparation
      ↓
Image Annotation
      ↓
Model Training
      ↓
Validation
      ↓
Testing
      ↓
Deployment
      ↓
Real-Time Detection
```

The custom model allows the system to be adapted to the specific objects and requirements of the project instead of relying only on generic pre-trained object classes.

---

# 🦾 Robotic Arms

The system contains **two robotic arms**.

Each arm uses:

* 6 Servo Motors
* Arduino-based control
* Centralized control logic

### Total Servo Motors

```text
Robotic Arm 1 → 6 Servo Motors
Robotic Arm 2 → 6 Servo Motors
--------------------------------
Total         → 12 Servo Motors
```

The robotic arms can receive commands from the main control system and perform predefined or AI-driven movements.

---

# 🎮 Robot Control System

One of the main features of the project is that the robot can be controlled using **three different methods**.

### Control Method 1 — AI / Autonomous Control

The AI system detects objects using the camera and object-detection models.

```text
Camera
 ↓
YOLO 11 / Custom AI
 ↓
Object Detection
 ↓
Decision
 ↓
Robot Command
 ↓
Robotic Arms
```

This allows the robot to perform intelligent actions based on the detected environment.

---

### Control Method 2 — Dedicated Application

A dedicated application was developed to provide direct control of the robotic system.

The application provides an interface through which the user can send commands to the robot and control its operation.

### 📱 Application Preview

> **Add your application screenshot here**

```text
![Robot Control Application](images/application.png)
```

You can replace the image path above with the actual location of your application screenshot.

---

### Control Method 3 — Manual / Hardware Control

The robotic system can also be controlled through the hardware control interface.

This provides an additional control method independent from the AI system and application.

---

# 🧩 Control Architecture

```text
                    ┌─────────────────────┐
                    │      AI System      │
                    │  YOLO 11 + Custom   │
                    │       Model         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Main Controller   │
                    │                     │
                    │    Arduino Nano     │
                    └──────────┬──────────┘
                               │
                 ┌─────────────┴─────────────┐
                 │                           │
                 ▼                           ▼
        ┌─────────────────┐        ┌─────────────────┐
        │  Robotic Arm 1  │        │  Robotic Arm 2  │
        │   6 Servos      │        │   6 Servos      │
        └─────────────────┘        └─────────────────┘

                 ▲
                 │
        ┌────────┴────────┐
        │ Control Methods │
        │                 │
        │ AI              │
        │ Application     │
        │ Manual Control  │
        └─────────────────┘
```

---

# 🔐 Security System

The project includes a dedicated **RFID-based security system** to protect access to the robotic system.

## RFID Authentication

When an RFID card/tag is presented to the system:

### Correct RFID ID

```text
RFID Detected
     ↓
ID Verification
     ↓
ID Correct
     ↓
Access Granted
     ↓
Door Opens
```

### Incorrect RFID ID

If the RFID ID is incorrect, the system requests a password.

```text
RFID Detected
     ↓
ID Incorrect
     ↓
Password Required
     ↓
Password Verification
```

If the password is entered incorrectly, the system continues its security procedure.

After the configured number of failed attempts, the system enters a security lockout state.

### Security Lockout

After repeated failed authentication attempts:

```text
Failed Authentication
        ↓
Attempt Limit Reached
        ↓
System Lock
        ↓
3-Hour Lockout
```

The system remains locked for **three hours** as a security measure.

---

# 🔄 System Reset

A physical **RESET button** is installed on the control system.

The reset button allows the operator to reset the system and return the controller to its initial operating state.

```text
RESET Button
     ↓
Controller Reset
     ↓
System Initialization
     ↓
Normal Operation
```

---

# 🌡️ Sensors & Monitoring

The project integrates several sensors for environmental and safety monitoring.

## 🌡️ DHT Sensor

The DHT sensor is used to monitor environmental conditions such as:

* Temperature
* Humidity

The sensor data can be processed by the controller and used for monitoring the operating environment.

---

## 🔥 Flame Sensor

A flame sensor is integrated into the system to detect the presence of a flame/fire condition.

```text
Flame Sensor
     ↓
Detection
     ↓
Controller
     ↓
Safety Response
```

---

## 🫧 Gas Sensor

A gas sensor is included for detecting the presence of potentially hazardous gases.

The sensor provides an additional safety layer for the robotic/control system.

```text
Gas Sensor
    ↓
Gas Detection
    ↓
Arduino
    ↓
Monitoring / Alert
```

---

# ⚡ Power Monitoring System

The system is powered using **two power supplies**.

A voltage monitoring section was integrated into the control box to monitor the power system.

The system measures the voltage from both power supplies and calculates the **average voltage**.

### Power Monitoring Concept

```text
Power Supply 1 ─────┐
                    │
                    ├──► Voltage Measurement
                    │
Power Supply 2 ─────┘
                           ↓
                     Average Voltage
                           ↓
                    System Monitoring
```

The voltage measurement provides a quick indication of the current power condition of the system.

---

# 🧠 Control Box

The project includes a dedicated **control box** containing the main electronics responsible for controlling the robotic system.

The control box contains the main embedded controller and the supporting electronic circuitry.

### Main Controller

**Arduino Nano**

The Arduino Nano is responsible for controlling the servo motors and interfacing with the robotic-arm control system.

---

# 🔧 Custom PCB Design

One of the major parts of the project is the development of **custom PCBs**.

The PCB designs were created specifically for this project rather than relying entirely on commercially available breadboards or development boards.

The PCB design process includes:

```text
System Requirements
       ↓
Circuit Design
       ↓
Schematic
       ↓
PCB Layout
       ↓
Routing
       ↓
Design Verification
       ↓
PCB Fabrication
       ↓
Assembly
       ↓
Testing
```

### PCB Design

> **Add PCB design images here**

```text
![PCB Design](images/pcb-design.png)
```

Additional PCB images can be added:

```text
![PCB Front](images/pcb-front.png)

![PCB Back](images/pcb-back.png)

![PCB Assembly](images/pcb-assembly.png)
```

---

# 🧰 Hardware Components

| Component                       |    Quantity | Purpose                           |
| ------------------------------- | ----------: | --------------------------------- |
| Arduino Nano                    |           1 | Main robotic control              |
| Servo Motors                    |          12 | Two robotic arms                  |
| Robotic Arms                    |           2 | Object manipulation               |
| DHT Sensor                      |          1+ | Temperature & humidity monitoring |
| Flame Sensor                    |          1+ | Flame detection                   |
| Gas Sensor                      |          1+ | Gas detection                     |
| RFID System                     |           1 | Security & authentication         |
| RFID Tags/IDs                   | As required | User authentication               |
| Power Supplies                  |           2 | System power                      |
| Voltmeter / Voltage Measurement |           1 | Power monitoring                  |
| Reset Button                    |           1 | System reset                      |
| Custom PCBs                     |    Multiple | System electronics                |

---

# 💻 Software & Libraries

The project uses a combination of AI, computer-vision, embedded-system, and application-development technologies.

## Artificial Intelligence

* **YOLO 11**
* Custom-trained AI model
* Object Detection
* Computer Vision
* Model Training & Validation

## Embedded Development

* Arduino IDE
* Arduino Nano
* Servo motor control
* Sensor interfacing
* RFID communication

## Main Libraries

> Add/remove libraries here according to the exact source code used in the final version.

```text
Servo
MFRC522
DHT sensor library
Adafruit Unified Sensor
```

### AI / Computer Vision Libraries

Depending on the final implementation:

```text
Ultralytics
OpenCV
NumPy
PyTorch
```

### Application

The project also includes a dedicated control application used to communicate with and control the robotic system.

> **Application source / download link:**

```text
[ADD APPLICATION URL HERE]
```

---

# 📁 Project Structure

A recommended GitHub repository structure is:

```text
Project/
│
├── README.md
│
├── AI/
│   ├── dataset/
│   ├── models/
│   ├── training/
│   └── detection/
│
├── Arduino/
│   ├── main_controller/
│   ├── robotic_arm_1/
│   ├── robotic_arm_2/
│   └── sensors/
│
├── Application/
│   ├── source/
│   └── assets/
│
├── PCB/
│   ├── schematic/
│   ├── pcb/
│   └── manufacturing/
│
├── Hardware/
│   ├── wiring/
│   └── diagrams/
│
├── Documentation/
│   └── images/
│
└── LICENSE
```

---

# 🔄 Complete System Workflow

The complete system operates through multiple integrated stages.

```text
                   ┌──────────────┐
                   │    Camera    │
                   └──────┬───────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │     YOLO 11     │
                 │       +         │
                 │   Custom Model  │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Object Detection│
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Decision / Logic│
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │  Arduino Nano   │
                 └────────┬────────┘
                          │
             ┌────────────┴────────────┐
             ▼                         ▼
      ┌──────────────┐          ┌──────────────┐
      │ Robotic Arm 1│          │ Robotic Arm 2│
      │   6 Servos   │          │   6 Servos   │
      └──────────────┘          └──────────────┘
```

At the same time, the monitoring and security subsystems operate alongside the robotic control system:

```text
DHT Sensor ───────┐
Flame Sensor ─────┤
Gas Sensor ───────┤
RFID Security ────┤
Voltage Monitor ──┤
Reset Button ─────┤
                  ▼
             Control System
```

---

# 🛡️ Security Workflow

```text
                RFID Scan
                    │
                    ▼
             ┌─────────────┐
             │ Valid ID ?  │
             └──────┬──────┘
                 YES│   │NO
                    │   │
                    ▼   ▼
               Door Open
                        │
                        ▼
                 Password Input
                        │
                        ▼
                 ┌─────────────┐
                 │ Password OK?│
                 └──────┬──────┘
                    YES │ NO
                        │
                        ▼
                  Failed Attempts
                        │
                        ▼
                  Limit Reached
                        │
                        ▼
                 3-Hour Lockout
```

---

# 📊 System Analysis

The project can be divided into several major engineering subsystems:

| Subsystem     | Main Technology               | Function               |
| ------------- | ----------------------------- | ---------------------- |
| AI            | YOLO 11 + Custom AI           | Object detection       |
| Vision        | Camera + Computer Vision      | Environment perception |
| Control       | Arduino Nano                  | Embedded control       |
| Robotics      | 12 Servo Motors               | Two robotic arms       |
| Application   | Dedicated Control App         | User control           |
| Security      | RFID + Password               | Access protection      |
| Environmental | DHT                           | Temperature/Humidity   |
| Safety        | Flame Sensor                  | Flame detection        |
| Safety        | Gas Sensor                    | Gas detection          |
| Power         | Dual PSU + Voltage Monitoring | Power supervision      |
| Electronics   | Custom PCBs                   | Hardware integration   |
| Reset         | Physical Button               | System reset           |

---

# 🚀 Development Progress

The project was developed through multiple stages.

## Phase 1 — System Concept

* Defined the overall robotic system.
* Determined the required robotic functions.
* Planned the AI and hardware architecture.
* Defined the two-arm configuration.

## Phase 2 — Robotic Arms

* Integrated the first robotic arm.
* Integrated the second robotic arm.
* Added six servo motors to each arm.
* Developed the servo-control system.

**Current configuration:**

```text
2 Robotic Arms
12 Servo Motors
6 Servos / Arm
```

## Phase 3 — Embedded Control

* Added Arduino Nano to the control box.
* Developed the central control logic.
* Integrated the servo system.
* Integrated sensors and supporting electronics.

## Phase 4 — AI Integration

* Integrated YOLO 11.
* Developed the computer-vision pipeline.
* Developed a custom AI model.
* Trained the model for project-specific object detection.
* Connected object detection with the robotic workflow.

## Phase 5 — Application Development

* Developed a dedicated control application.
* Added direct robot-control functionality.
* Integrated the application with the robotic system.

## Phase 6 — Security System

* Added RFID authentication.
* Implemented valid-ID access.
* Added password authentication for invalid RFID attempts.
* Implemented failed-attempt handling.
* Added a three-hour security lockout.
* Added a physical reset button.

## Phase 7 — Sensors & Safety

* Added DHT environmental monitoring.
* Added flame detection.
* Added gas detection.
* Integrated the sensors into the control system.

## Phase 8 — Power Monitoring

* Integrated two power supplies.
* Added voltage measurement.
* Implemented average-voltage monitoring.
* Added power-status monitoring to the control system.

## Phase 9 — PCB Development

* Designed custom PCBs.
* Created the electronic layouts.
* Integrated the different system components.
* Prepared the electronics for a more organized and reliable final system.

---

# 📈 Current System Status

The project currently integrates:

```text
                 INTELLIGENT ROBOTIC SYSTEM
                           │
       ┌───────────────────┼───────────────────┐
       │                   │                   │
       ▼                   ▼                   ▼
      AI                Robotics           Security
       │                   │                   │
 YOLO 11             2 Robotic Arms       RFID
 Custom Model        12 Servo Motors      Password
       │                   │              Lockout
       │                   │                   │
       └───────────────────┼───────────────────┘
                           │
                           ▼
                    Arduino Nano
                           │
       ┌───────────────────┼───────────────────┐
       │                   │                   │
       ▼                   ▼                   ▼
    Sensors             Power             Application
       │               Monitoring              │
       │                   │                   │
 DHT / Flame / Gas    2 Power Supplies      Control
                           │
                     Average Voltage
```

---

# 🧪 Testing

The system should be tested across multiple categories:

### AI Testing

* Object detection accuracy
* Detection under different lighting conditions
* Detection distance
* False detections
* Real-time performance

### Robotic Testing

* Servo movement accuracy
* Arm positioning
* Repeatability
* Communication reliability
* Maximum operating load

### Security Testing

* Valid RFID
* Invalid RFID
* Correct password
* Incorrect password
* Repeated failed attempts
* Three-hour lockout
* Reset functionality

### Sensor Testing

* DHT readings
* Flame detection
* Gas detection
* Sensor response time

### Power Testing

* Power supply voltage
* Average voltage
* Voltage stability
* System behavior under load

---

# 📷 Project Images

## Complete System

> Add your main project image here.

```text
![Complete Robotic System](images/project.jpg)
```

## Control Box

```text
![Control Box](images/control-box.jpg)
```

## Robotic Arms

```text
![Two Robotic Arms](images/robotic-arms.jpg)
```

## AI Detection

```text
![AI Object Detection](images/ai-detection.jpg)
```

## Application

```text
![Control Application](images/application.png)
```

## PCB

```text
![Custom PCB](images/pcb.jpg)
```

---

# 🎥 Demo

> Add your project demonstration video here.

```text
[ADD DEMO VIDEO URL HERE]
```

---

# 🔗 Project Links

## AI Model

```text
[ADD AI MODEL URL HERE]
```

## Application

```text
[ADD APPLICATION URL HERE]
```

## Source Code

```text
[ADD SOURCE CODE URL HERE]
```

## PCB Design Files

```text
[ADD PCB FILES URL HERE]
```

## Project Documentation

```text
[ADD DOCUMENTATION URL HERE]
```

## Demonstration Video

```text
[ADD VIDEO URL HERE]
```

---

# 🛠️ Technologies Used

### Hardware

* Arduino Nano
* Servo Motors
* Robotic Arms
* RFID Module
* DHT Sensor
* Flame Sensor
* Gas Sensor
* Voltage Measurement
* Dual Power Supplies
* Custom PCBs
* Camera

### Software

* YOLO 11
* Custom AI Model
* Computer Vision
* Arduino IDE
* Python
* Dedicated Control Application

### AI / Computer Vision

* YOLO 11
* OpenCV
* PyTorch
* Ultralytics
* NumPy

### Embedded

* Arduino
* Servo Control
* RFID Communication
* Sensor Interfaces

---

# 🌟 Key Features

* ✅ Real-time AI object detection
* ✅ YOLO 11 integration
* ✅ Custom-trained AI model
* ✅ Two robotic arms
* ✅ 12 servo motors
* ✅ Three control methods
* ✅ Dedicated control application
* ✅ Arduino Nano control system
* ✅ RFID security
* ✅ Password authentication
* ✅ Failed-attempt protection
* ✅ Three-hour security lockout
* ✅ Physical reset button
* ✅ Temperature monitoring
* ✅ Humidity monitoring
* ✅ Flame detection
* ✅ Gas detection
* ✅ Dual power supplies
* ✅ Average voltage monitoring
* ✅ Custom PCB design
* ✅ Integrated hardware/software architecture

---

# 🔮 Future Improvements

Possible future improvements include:

* Higher-accuracy object detection
* Additional custom AI classes
* Improved robotic-arm trajectory planning
* Automatic object grasping
* More advanced inverse-kinematics control
* Remote monitoring
* Real-time system dashboard
* Database integration
* System event logging
* More advanced security features
* Improved power monitoring
* Additional safety sensors
* Mobile application support
* Autonomous task planning

---

# 👨‍💻 Project Development

This project was developed as an integrated engineering project combining:

**Artificial Intelligence + Computer Vision + Robotics + Embedded Systems + Electronics + PCB Design + Software Development + Security Systems.**

The main goal is not simply to build a robotic arm, but to create a complete intelligent robotic platform in which **AI perception, robotic movement, user control, safety monitoring, power management, and security work together as one system.**

---

# 📜 License

This project is intended for educational, research, and development purposes.

Add your preferred license here:

```text
[ADD LICENSE HERE]
```

---

# ⭐ Support

If you find this project useful or interesting, consider giving the repository a ⭐ on GitHub.

---

## 📌 Project Summary

```text
AI
│
├── YOLO 11
├── Custom AI Model
└── Object Detection
        │
        ▼
Control System
│
├── Arduino Nano
├── Application
└── Manual Control
        │
        ▼
Robotics
│
├── Robotic Arm 1 → 6 Servos
└── Robotic Arm 2 → 6 Servos
        │
        ▼
Safety & Monitoring
│
├── DHT Sensor
├── Flame Sensor
├── Gas Sensor
└── Voltage Monitoring
        │
        ▼
Security
│
├── RFID
├── Password
├── Failed Attempt Protection
├── 3-Hour Lockout
└── Reset System
        │
        ▼
Electronics
│
├── Dual Power Supplies
└── Custom Designed PCBs
```

**Built with AI, Robotics, Embedded Systems, Electronics, and Engineering. 🤖🧠⚙️**
