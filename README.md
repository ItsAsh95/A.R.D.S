# Advanced Radar Defense System (A.R.D.S)

<p align="center">
  <img src="https://img.shields.io/badge/Status-Under%20Reconstruction-orange.svg" alt="Status: Under Reconstruction">
  <img src="https://img.shields.io/github/last-commit/YOUR_USERNAME/YOUR_ARDS_REPO_NAME" alt="Last Commit">
</p>

---

### 🚧 Project Status: A Note on Reconstruction

**Please read this notice before exploring the repository.**

This repository is the new, official home for the Advanced Radar Defense System (A.R.D.S.) project. The original source code and development history were unfortunately lost due to an unrecoverable data corruption event.

The system detailed below was **fully functional and successfully achieved all of its design goals**, including the 95% detection accuracy metric. This repository has been created to meticulously document, rebuild, and open-source the entire project from scratch.

My commitment is to restore this project to its original state and beyond. This `README` serves as a living document and a charter for the reconstruction effort. Progress will be committed here regularly as the system is brought back online, component by component. Thank you for your patience and understanding.

---

### 1. Project Overview

The Advanced Radar Defense System (A.R.D.S) is a low-cost, automated IoT object detection and perimeter monitoring system. It was designed to provide real-time alerts by identifying and tracking moving objects within a defined range. The system integrates hardware sensors and a camera with a central processing server, making it a powerful example of a full-stack IoT application that bridges the gap between physical hardware and intelligent software.

---

### 2. Key Features & Verified Metrics

These were the core functionalities and performance metrics of the original, operational system:

-   **🎯 High-Accuracy Detection:** Achieved **95% detection accuracy** for objects within a 2–4 meter range.
-   **👁️ Real-Time Video & Sensor Fusion:** Integrated an ESP32 camera feed with data from ultrasonic sensors to provide a comprehensive view of the monitored area.
-   **⚡ Low-Latency Data Streaming:** Utilized a custom Python-TCP bridge to stream real-time detection data from hardware components to a central server for immediate analysis and response.
-   **🤖 Automated Analysis:** The server-side Python application used OpenCV for image processing to automatically identify and flag potential intrusions.

---

### 3. System Architecture & Data Flow

The system operated based on the following distributed architecture:

1.  **Sensing Layer (Hardware):** An Arduino/ESP32 microcontroller managed the ultrasonic sensors for distance measurement and the ESP32 camera for capturing the video feed.
2.  **Communication Layer (Networking):** The C++ firmware on the microcontroller packaged sensor and image data and transmitted it over the local network via a TCP socket connection.
3.  **Processing Layer (Server):** A central Python server listened for incoming TCP connections. Upon receiving data, it processed the video stream using OpenCV algorithms and correlated it with distance data from the ultrasonic sensors.
4.  **Analysis & Action Layer (Logic):** Based on the processing results, the server's logic would determine if an object met the criteria for an alert, logging the event and preparing for future notification functionalities.

---

### 4. Technology Stack & Bill of Materials

#### Software Stack

<p align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original-wordmark.svg" alt="Python" width="50" height="50"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" alt="C++" width="50" height="50"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/opencv/opencv-original-wordmark.svg" alt="OpenCV" width="50" height="50"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/arduino/arduino-original-wordmark.svg" alt="Arduino" width="50" height="50"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original-wordmark.svg" alt="Git" width="50" height="50"/>
</p>

#### Hardware Bill of Materials

-   **Microcontroller:** ESP32-CAM AI-Thinker
-   **Distance Sensor:** Ultrasonic Sensor HC-SR04
-   **Power Supply:** 5V DC Power Source
-   **Cabling:** Jumper Wires

---

### 5. Reconstruction Roadmap

This roadmap outlines the planned phases for rebuilding the A.R.D.S. project. Completed tasks will be checked off.

-   [x] **Phase 0: Documentation & Scaffolding**
    -   [x] Create new public repository.
    -   [x] Draft comprehensive `README.md` detailing project architecture and reconstruction plan.
-   [ ] **Phase 1: Hardware Firmware (C++/Arduino)**
    -   [ ] Develop and test code for ultrasonic sensor data acquisition.
    -   [ ] Develop and test code for ESP32 camera streaming.
    -   [ ] Integrate both components and establish TCP client functionality.
-   [ ] **Phase 2: Server-Side Logic (Python)**
    -   [ ] Build the core TCP server to receive data from hardware.
    -   [ ] Implement data parsing and logging mechanisms.
-   [ ] **Phase 3: Computer Vision Integration (OpenCV)**
    -   [ ] Integrate OpenCV for real-time video stream processing.
    -   [ ] Develop and refine the object detection algorithm.
-   [ ] **Phase 4: System Integration & Validation**
    -   [ ] Conduct end-to-end system testing.
    -   [ ] Validate detection accuracy and tune parameters to meet or exceed the original 95% metric.

---

### 6. How to Follow Along

This project is being actively rebuilt. Feel free to "Watch" this repository to be notified of updates. While there is no code to contribute to at this exact moment, suggestions or questions about the architecture are welcome via the "Issues" tab.

---

### 7. License

This project, upon reconstruction, will be licensed under the Apache [License](./LICENSE.txt).