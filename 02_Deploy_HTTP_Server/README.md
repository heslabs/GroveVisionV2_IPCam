# Deploy a Http Server With XIAO ESP32C3 Sense

### Step 1: Download and install Arduino IDE
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
### Step 2: Download the SSCMA package and upload to Arduino IDE
* Download SSCMA zip package from Seeed-Studio [[GitHub]](<https://github.com/Seeed-Studio/Seeed_Arduino_SSCMA>)
* Download file: Seeed_Arduino_SSCMA-main.zip
* 
<img src="https://github.com/user-attachments/assets/633508a4-18f5-4f8b-bf3a-5ee567f2ecb3" width=550>

* Launch Arduino IDE and upload this package (zip file) to Arduino IDE
<img src="https://github.com/user-attachments/assets/a861f634-a988-4568-9dbe-ba9699b05c23" width=550>

* It takes a few minutes to complete the installation.
<img src="https://github.com/user-attachments/assets/ed8109f1-0f6c-4fff-840b-0897950f5b12" width=550>

---
### Step 3: Open camera web server demo program and set your 2.4G wifi 

* Open camera web server demo
  * Files -> Examples -> Seeed Arduino -> Camera Web Server
<img src="https://github.com/user-attachments/assets/fd4805d2-d62d-4ee2-a383-de40d8c67f38" width=550>

* Set your 2.4G wifi ssid and password
  * Please pay attention to 2.4G wifi, not 5G
<img src="https://github.com/user-attachments/assets/1dfb0d66-a647-4662-9b98-44fbc2f475a0" width=550>

---
### Step 4: Upload it to ESP32SC3
* Connect your board by USB type-c cable
<img src="https://github.com/user-attachments/assets/40343e8a-9615-4150-b896-11c1d85b4ccb" width=150>

* Click the “Select Board” window and choose the tab ”Select other Board and Port”
<img src="https://github.com/user-attachments/assets/c35835b6-d180-4d92-a732-6bbea2dc14f5" width=550>

* Scroll down to select: Board (XIAO_ESP32C3) and Port (/dev/ttyACM0)
<img src="https://github.com/user-attachments/assets/2ce5b4fb-47b0-48e7-b94e-f4c968d8c33b" width=550>

---
### Step 5: Install required libraries in Arduino IDE
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
### Step 6: Running AI model run successfully in your browser

First, you need to make sure your computer is on the same LAN with Grove Vision AI V2. 
Open your browser and input the ip address you got from the previous step and click Start Stream button. You will see the AI model run successfully in your browser.

<img src="https://github.com/user-attachments/assets/ca13daff-7460-44aa-89d2-1bbf03b7884f" width=650>
