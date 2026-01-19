# Grove Vision AI v2 - IP Camera 
## Quick Start Guide

1. Upload AI Model to Grove Vision AI V2 [[Pages]](<https://github.com/heslabs/GroveVisionV2_IPCam/tree/main/01_Upload_AI_Model>)
2. Deploy a Http Server With XIAO ESP32C3 Sense [[Pages]](<https://github.com/heslabs/GroveVisionV2_IPCam/tree/main/02_Deploy_HTTP_Server>)

---
### Overview

This lab will use the off-the-shelf silicon devices and cost-effective evaluation board from Himax Seeed Studio.
 
Intelligent IP Camera with AI Function
Reference: Seeed Studio - Intelligent IP Camera With AI Function [[wiki]](<https://wiki.seeedstudio.com/grove_vision_ai_v2_webcamera>)
* Grove Vision AI V2 can be advanced surveillance devices that integrate artificial intelligence to enhance security and operational efficiency.
* * These cameras can perform real-time video analysis to detect and alert for unusual activities, recognize faces, and monitor crowd density, making them ideal for applications in areas such as public safety, retail management, and smart home security. 

<img src="https://github.com/user-attachments/assets/1e7524ca-aee3-40bf-a880-ab9c8a21ea03" width=600>

---
### Prerequisites

For this tutorial, the following hardware modules are required
* Grove Vision AI V2 [[Buy]](https://www.seeedstudio.com/Grove-Vision-AI-Module-V2-p-5851.html)
* Raspberry Pi OV5647 Camera Module [[more]](<https://www.seeedstudio.com/Grove-Vision-AI-V2-Kit-p-5852.html>)
* Seeed Studio XIAO ESP32C3 (2.4GHz WiFi, BLE 5.0) [[more]](<https://www.seeedstudio.com/XIAO-ESP32S3-Sense-p-5639.html>)
  
<img src="https://github.com/user-attachments/assets/a6df1caf-ea49-46f3-98fe-864cfaf54020" width=450>

<img src="https://github.com/user-attachments/assets/6c196752-b67e-4665-af6b-52e564f15ff0" width=350>

#### Grove Vision AI V2 Kit (with Camera & XIAO) +$28.88 [[Online Store]](<https://www.seeedstudio.com/Grove-Vision-AI-V2-Kit-p-5852.html>)

<img src="https://github.com/user-attachments/assets/bd7f12c7-3ae0-488a-bdf7-2bcb80faef4a" width=350>

---
### Grove Vision AI Module V2
Reference: [[Seeedstudio Wiki page]](<https://wiki.seeedstudio.com/grove_vision_ai_v2>)

* It is an MCU-based vision AI module powered by Arm Cortex-M55 & Ethos-U55. It supports TensorFlow and PyTorch frameworks and is compatible with Arduino IDE. With the SenseCraft AI algorithm platform, trained ML models can be deployed to the sensor without the need for coding.
* It features a standard CSI interface, an onboard digital microphone and an SD card slot, making it highly suitable for various embedded AI vision projects.

---
### Seeed Studio XIAO ESP32C3
Reference:[[Seeedstudio Wiki page]](< https://wiki.seeedstudio.com/XIAO_ESP32C3_Getting_Started>)

* CPU: ESP32-C3, 32­bit RISC­-V single core processor that operates at up to 160 MHz
* Complete Wi­Fi subsystem: Complies with IEEE 802.11b/g/n protocol and supports Station mode, SoftAP mode, SoftAP + Station mode, and promiscuous mode
* Bluetooth LE subsystem: Supports features of Bluetooth 5 and Bluetooth mesh
* Ultra-Low Power: Deep sleep power consumption is about 43μA

---
### Himax WiseEye2 AI Processor (WE2)
Reference: [[Himax product page]](<https://www.himax.com.tw/products/wiseeye-ai-sensing/wiseeye2-ai-processor>)
  
* WiseEye2 (WE2 AI solution) AI solution is composed of two components: an ultralow power CMOS image sensor and an AI microcontroller HX6538 WE2.  
* The WE2 features Arm based Cortex M55 CPU and Ethos U55 NPU, rich sets of sensor control interfaces, industrial grade security and cryptography engines, and multi-layer power management architecture.  

---
### Lab setup for Ethernet and USB connection
* IP Camera (Ethernet connection)
* SenseCraft-Web-Toolkit (USB connection)

<img src="https://github.com/user-attachments/assets/1c1768d6-6fb5-482b-a605-10590ed0d8d7" width=650>

---
### Grove Vision AI V2 - Web Camera Example

<img src="https://github.com/user-attachments/assets/e98aa65d-245e-45f8-9d20-0c748823256b" width=650>
<img src="https://github.com/user-attachments/assets/c778a4be-9314-40e5-b615-3c2b9d96e291" width=650>

---
### Arm Corstone Subsystem

* The Grove Vision V2 is based on Arm Cortex-M55 and Ethos-U55 platform in the Arm Corstone-300 subsystem IP
* Arm Corstone is designed as the foundation for an efficient, high-performance SoC and includes a reference design to efficiently integrate Arm IPs with power, clock, debug, and security infrastructure. 

<img src="https://github.com/user-attachments/assets/525e578d-f26c-46f5-99ab-f1bca6d77d89" width=750>

<img src="https://github.com/user-attachments/assets/065f2b7e-d60e-435c-9a09-f4ba0f13a7f5" width=750>

#### Arm Cortex-M55 Processor 
* Reference: [[Arm Developer Pages]](<https://developer.arm.com/documentation/101051/0101/?lang=en>)
* The Cortex-M55 processor is the first Arm Cortex-M processor supporting the Armv8.1-M architecture. With Arm Helium technology (also known as the M-Profile Vector Extension, MVE).

#### Arm Ethos-U55 NPU [more]
* Reference: [[Arm Developer Pages]](<https://developer.arm.com/Processors/Ethos-U55>)
* The Neural Processing Unit (NPU) improves the inference performance of neural networks. The NPU targets 8-bit and 16-bit integer quantized Convolutional Neural Networks (CNN) and Recurrent Neural Networks (RNN). The NPU supports 8-bit weights.

---
### Arm Ethos-U NPU 
Reference: Arm Ethos-U NPU — Comparison Table Comparison Table [[PDF]](<https://armkeil.blob.core.windows.net/developer/Files/pdf/datasheets/arm-ethos-u-processor-series-product-brief.pdf>)

<img src="https://github.com/user-attachments/assets/3b9837aa-25a4-42c1-abdc-9558b73f1eef" width=550>

---
### Arm IoT Reference Design Platform  
Reference: Arm IoT Reference Design Platform Comparison Table [[PDF]](<https://documentation-service.arm.com/static/6614bbed1bc22b03bca93570?token=>)

<img src="https://github.com/user-attachments/assets/797137ed-3a74-4087-b679-80a5bbe6121c" width=950>

---
### 2024 MCU AI Vision Boards: Performance Comparison
https://www.hackster.io/limengdu0117/2024-mcu-ai-vision-boards-performance-comparison-998505

---
### Computer Vision at the Edge with Grove Vision AI Module V2
https://www.hackster.io/mjrobot/computer-vision-at-the-edge-with-grove-vision-ai-module-v2-0003c7?f=1&fbclid=IwAR0X54tBQe_i3DYQgmUaJH725mWhL2qpiAeGNdEALYN4BQ7cXuOOPRMRJYU

---
<img src="https://github.com/user-attachments/assets/044e1c60-189a-4e53-bf4b-ea9c3eb2cf54" width=1050>

---
<img src="https://github.com/user-attachments/assets/31600c02-0b78-44cc-bca7-fc99c3ba131a" width=1050>

