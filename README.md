# 📸 Send Image via WhatsApp using ESP32-CAM

This project demonstrates how to capture an image using the ESP32-CAM and send it directly to WhatsApp using a cloud API. It combines embedded systems, IoT, and real-time communication into a single smart application.

---

## 🚀 Overview

In today’s world, instant communication is essential. This project extends that concept beyond smartphones by enabling a microcontroller (ESP32-CAM) to capture images and send them directly to WhatsApp.

Whenever a push button is pressed, the ESP32-CAM captures an image and sends it instantly to a predefined WhatsApp number using the CircuitDigest Cloud API.

---

## 🧰 Components Required

- ESP32-CAM (with or without USB interface)
- Push Button
- Breadboard
- Jumper Wires
- 5V Power Supply / USB Cable

---

## 🔌 Circuit Description

- Push button connected to **GPIO13**
- Other terminal connected to **GND**
- Internal pull-up resistor used in code
- Flash LED connected to **GPIO4**

When the button is pressed, it triggers image capture.

---

## ⚙️ Working Principle

1. ESP32-CAM connects to WiFi
2. Waits for button press
3. On press:
   - Flash LED turns ON
   - Image is captured
   - Image is sent via WhatsApp using API
4. Message includes:
   - Image
   - Timestamp
   - Device info

---

## 💻 Source Code Structure

The code is divided into key functional parts:

- **Initialization** → WiFi & Camera setup  
- **Image Capture** → Capture and store image buffer  
- **Memory Handling** → Efficient buffer allocation  
- **API Communication** → HTTPS POST request  
- **Main Loop** → Button detection & triggering  

---

## 🔐 Configuration

Update the following in your code:

```cpp
const char *ssid = "YOUR_SSID";
const char *pwd = "YOUR_PASSWORD";
const char *apiKey = "YOUR_API_KEY";
const char *phone = "YOUR_PHONE_NUMBER";

---

##  **Author**
Vedhathiri.K 
