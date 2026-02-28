# 📶 Quectel EC200U-CN WebUI
**Created by [MisterNegative](https://github.com/MISTERNEGATIVE21)**

Welcome! This repository provides a complete Web User Interface (WebUI) for the **Quectel EC200U-CN** LTE Cat 1 module. By using this setup, you can monitor network status, manage SMS, and control your module directly from a web browser, all powered by your Arduino board.

---

## 📸 Demo Preview

*(Upload your images to a folder named `images` in your repository to make these links work)*

![WebUI Home Dashboard](images/demo_home.png)
> **Figure 1:** The main dashboard showing signal strength, network operator, and live connection status.

![GPS & SMS Interface](images/demo_gps.png)
> **Figure 2:** WebUI interface displaying live GPS coordinates and SMS management.

---

## 🚀 Step 1: Download the Library & WebUI Assets

To get the required WebUI files and the Arduino library for your module, please navigate directly to the main library repository:

👉 **[https://github.com/MISTERNEGATIVE21/QuectelEC200U](https://github.com/MISTERNEGATIVE21/QuectelEC200U)**

There you will find the library release and all necessary files to interface your Quectel EC200U-CN with Arduino.

---

## 🔌 Step 2: Arduino Hardware Setup

Connect your Arduino (e.g., ESP32, Arduino Mega) to the EC200U-CN module.

| EC200U-CN Pin | Arduino Pin (ESP32 Example) | Description |
| :--- | :--- | :--- |
| **TX** | **RX (Pin 16)** | Transmits data to Arduino |
| **RX** | **TX (Pin 17)** | Receives data from Arduino |
| **GND** | **GND** | Common Ground |
| **VBAT** | **External 3.8V-4.2V Power** | Do NOT use Arduino 5V! |

> **⚠️ Important:** The EC200U-CN uses 1.8V logic. If you are using a 5V Arduino board (like the Uno), you **must** use a logic level shifter on the TX/RX lines to prevent damaging the module.

---

## 📝 Step 3: Running the WebUI Example Code

Once you have downloaded and installed the `QuectelEC200U` library from the link above, you can use the pre-built example to get started instantly!

1. In the Arduino IDE, go to **File** -> **Examples** -> **QuectelEC200U**.
2. Select the **`Webui`** example sketch.
3. Check the pin definitions at the top of the sketch to ensure they match your hardware wiring.
4. Click **Upload** to flash the code to your Arduino board.
5. Open the **Serial Monitor** (set to 115200 baud) to watch the initialization process. 

---

## 🌐 Accessing the WebUI

1. Once the Arduino code says the modem is initialized and the WebUI is running, connect your PC or phone to the module's network (via USB RNDIS/ECM or Wi-Fi if bridging).
2. Open your web browser.
3. Navigate to the module's local IP address (usually `http://192.168.1.1` or `http://192.168.225.1`).
4. You should now see the WebUI dashboard!

---

## 🤝 Contributing & Support
If you find a bug or want to add a new feature to the WebUI or the `QuectelEC200U` library, feel free to open an Issue or submit a Pull Request!
