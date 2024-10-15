# Grove Vision AI v2 - IP Camera 
## Quick Start Guide

---
### Overview

This lab will use the off-the-shelf silicon devices and cost-effective evaluation board from Himax Seeed Studio.
 
Intelligent IP Camera With AI Function
* Reference: Seeed Studio - Intelligent IP Camera With AI Function
    * https://wiki.seeedstudio.com/grove_vision_ai_v2_webcamera/

Grove Vision AI V2 can be advanced surveillance devices that integrate artificial intelligence to enhance security and operational efficiency. These cameras can perform real-time video analysis to detect and alert for unusual activities, recognize faces, and monitor crowd density, making them ideal for applications in areas such as public safety, retail management, and smart home security. 

<img src="https://github.com/user-attachments/assets/1e7524ca-aee3-40bf-a880-ab9c8a21ea03" width=600>

---
### Prerequisites

For this tutorial, the following hardware modules are required
* Grove Vision AI V2 Kit [[more]](<https://www.seeedstudio.com/Grove-Vision-AI-V2-Kit-p-5852.html>)
    * Grove Vision AI V2 module
    * Raspberry Pi OV5647 camera module 
* XIAO ESP32C3 WIFI module [[more]](<https://www.seeedstudio.com/XIAO-ESP32S3-Sense-p-5639.html>)


<img src="https://github.com/user-attachments/assets/a6df1caf-ea49-46f3-98fe-864cfaf54020" width=450>

<img src="https://github.com/user-attachments/assets/6c196752-b67e-4665-af6b-52e564f15ff0" width=350>

---
## Grove Vision AI Module V2
* Reference: https://wiki.seeedstudio.com/grove_vision_ai_v2/ 

It is an MCU-based vision AI module powered by Arm Cortex-M55 & Ethos-U55. It supports TensorFlow and PyTorch frameworks and is compatible with Arduino IDE. With the SenseCraft AI algorithm platform, trained ML models can be deployed to the sensor without the need for coding. It features a standard CSI interface, an onboard digital microphone and an SD card slot, making it highly suitable for various embedded AI vision projects.

<img src="https://github.com/user-attachments/assets/18923aed-57eb-4f2f-a045-77cfce858c1d" width=400>

---
### Seeed Studio XIAO ESP32C3
* Reference: https://wiki.seeedstudio.com/XIAO_ESP32C3_Getting_Started/ 

CPU: ESP32-C3, 32­bit RISC­-V single core processor that operates at up to 160 MHz
Complete Wi­Fi subsystem: Complies with IEEE 802.11b/g/n protocol and supports Station mode, SoftAP mode, SoftAP + Station mode, and promiscuous mode
Bluetooth LE subsystem: Supports features of Bluetooth 5 and Bluetooth mesh
Ultra-Low Power: Deep sleep power consumption is about 43μA

---
### Himax WiseEye2 AI Processor (WE2)
* Reference: https://www.himax.com.tw/products/wiseeye-ai-sensing/wiseeye2-ai-processor/
  
WiseEye2 (WE2 AI solution) AI solution is composed of two components: an ultralow power CMOS image sensor and an AI microcontroller HX6538 WE2.  
The WE2 features Arm based Cortex M55 CPU and Ethos U55 NPU, rich sets of sensor control interfaces, industrial grade security and cryptography engines, and multi-layer power management architecture.  

---
### Arm Corstone Subsystem
Arm Corstone is designed as the foundation for an efficient, high-performance SoC and includes a reference design to efficiently integrate Arm IPs with power, clock, debug, and security infrastructure. 

<img src="https://github.com/user-attachments/assets/525e578d-f26c-46f5-99ab-f1bca6d77d89" width=750>

<img src="https://github.com/user-attachments/assets/065f2b7e-d60e-435c-9a09-f4ba0f13a7f5" width=750>

#### Arm Cortex-M55 Processor 
* https://developer.arm.com/documentation/101051/0101/?lang=en>
* The Cortex-M55 processor is the first Arm Cortex-M processor supporting the Armv8.1-M architecture. With Arm Helium technology (also known as the M-Profile Vector Extension, MVE).

#### Arm Ethos-U55 NPU [more]
* https://developer.arm.com/Processors/Ethos-U55
* The Neural Processing Unit (NPU) improves the inference performance of neural networks. The NPU targets 8-bit and 16-bit integer quantized Convolutional Neural Networks (CNN) and Recurrent Neural Networks (RNN). The NPU supports 8-bit weights.

---
### Upload AI Model to Grove Vision AI V2

#### Step 1. Connect the Grove Vision AI V2 to the SenseCraft AI Model Assistant

* Open the main SenseCraft AI Model Assistant page
  * https://seeed-studio.github.io/SenseCraft-Web-Toolkit 
* Please use a Type-C type cable to connect Grove Vision AI V2 to your computer.

<img src="https://github.com/user-attachments/assets/cf7cebca-7717-4d34-81d4-e15ec145531d" width=650>

* Change the permissions on serial port /dev/ttyACM*
 ``` $ sudo chmod 666 /dev/ttyACM* ```

#### Step 2. Upload a test AI model
* Select a model you want to use and click the Send button below.  It takes a few minutes to flash the memory of the device.

<img src="https://github.com/user-attachments/assets/4ef8edaa-d7b2-41d1-ad0a-0cb6d7421089" width=650>

#### Step 3. Observe the live video from camera in the preview window 
* Once the model is uploaded successfully, you will be able to see the live feed from the Grove Vision AI V2 camera in the Preview on the right.

<img src="https://github.com/user-attachments/assets/1b38062b-bba6-4670-9448-d736d7bf92fe" width=650>


---
### Deploy a Http Server With XIAO ESP32C3 Sense

#### Step 1: Download and install Arduino IDE
Optional if already installed
Reference: Download and install Arduino IDE [[Linux]](<https://support.arduino.cc/hc/en-us/articles/360019833020-Download-and-install-Arduino-IDE>) 
* Download the latest release for Linux OS [Download].
* Make the AppImage file executable.
* Execute AppImage file to launch Arduino IDE.
  ```
  $ chmod +x arduino-ide_latest_Linux_64bit.AppImage
  $ ./arduino-ide_latest_Linux_64bit.AppImage
  ```
<img src="https://github.com/user-attachments/assets/4fef079e-64f3-42c0-9598-211e7960163f" width=550>

---
#### Step 2: Download the SSCMA package and upload to Arduino IDE
* Download SSCMA zip package from Seeed-Studio [[GitHub]](<https://github.com/Seeed-Studio/Seeed_Arduino_SSCMA>)
* Download file: Seeed_Arduino_SSCMA-main.zip
* 
<img src="https://github.com/user-attachments/assets/633508a4-18f5-4f8b-bf3a-5ee567f2ecb3" width=550>

* Launch Arduino IDE and upload this package (zip file) to Arduino IDE
<img src="https://github.com/user-attachments/assets/a861f634-a988-4568-9dbe-ba9699b05c23" width=550>

* It takes a few minutes to complete the installation.
<img src="https://github.com/user-attachments/assets/ed8109f1-0f6c-4fff-840b-0897950f5b12" width=550>

---
#### Step 3: Open camera web server demo program and set your 2.4G wifi 

* Open camera web server demo
  * Files -> Examples -> Seeed Arduino -> Camera Web Server
<img src="https://github.com/user-attachments/assets/fd4805d2-d62d-4ee2-a383-de40d8c67f38" width=550>

* Set your 2.4G wifi ssid and password
  * Please pay attention to 2.4G wifi, not 5G
<img src="https://github.com/user-attachments/assets/1dfb0d66-a647-4662-9b98-44fbc2f475a0" width=550>

---
#### Step 4: Upload it to ESP32SC3
* Connect your board by USB type-c cable
<img src="https://github.com/user-attachments/assets/40343e8a-9615-4150-b896-11c1d85b4ccb" width=150>

* Click the “Select Board” window and choose the tab ”Select other Board and Port”
<img src="https://github.com/user-attachments/assets/c35835b6-d180-4d92-a732-6bbea2dc14f5" width=550>

* Scroll down to select: Board (XIAO_ESP32C3) and Port (/dev/ttyACM0)
<img src="https://github.com/user-attachments/assets/2ce5b4fb-47b0-48e7-b94e-f4c968d8c33b" width=550>

---
#### Step 5: Install required libraries in Arduino IDE
Sketch > Include Library > Manage Libraries. In the "Filter your search..." box, type in following library names in the search query 
  * ArduinoJson
  * Eigen
  * FreeRTOS 

<img src="https://github.com/user-attachments/assets/3290da50-0eda-4552-9700-b32d7605f3af" width=650>

* Modify the include directory for FreeRTOS

<img src="https://github.com/user-attachments/assets/6e06323a-42eb-41ba-81a9-fc7376bf9741" width=650>

* Upload the program
<img src="https://github.com/user-attachments/assets/a48d02fd-460a-471f-911f-cd40afb8ce94" width=650>

---
#### Step 6: Running AI model run successfully in your browser

First, you need to make sure your computer is on the same LAN with Grove Vision AI V2. 
Open your browser and input the ip address you got from the previous step and click Start Stream button. You will see the AI model run successfully in your browser.

<img src="https://github.com/user-attachments/assets/ca13daff-7460-44aa-89d2-1bbf03b7884f" width=650>

---
### Lab setup for Ethernet and USB connection
* IP Camera (Ethernet connection)
* SenseCraft-Web-Toolkit (USB connection)

<img src="https://github.com/user-attachments/assets/1c1768d6-6fb5-482b-a605-10590ed0d8d7" width=650>

---
### Grove Vision AI V2 - Web Camera Example

<img src="https://github.com/user-attachments/assets/5a0d83f5-d62e-4a62-802e-3f97c850b3fe" width=450>

<img src="https://github.com/user-attachments/assets/00d2a0c7-b5b8-430f-b0ce-7033f4ad57ea" width=450>





