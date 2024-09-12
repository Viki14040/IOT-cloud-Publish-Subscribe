# IoT Cloud Publish and Subscribe Project with NodeMCU ESP8266

This project demonstrates an IoT solution using a NodeMCU ESP8266 microcontroller for publishing and subscribing to messages over a cloud platform. The microcontroller communicates with the cloud to control connected devices remotely using the Arduino IDE.

## Features

- **WiFi Connectivity**: Connects to a WiFi network to interact with the cloud.
- **Publish/Subscribe Model**: Sends and receives messages to control devices and monitor parameters.
- **Remote Control**: Allows device control via mobile or computer from anywhere with internet access.
- **Real-time Monitoring**: Monitors network status and controls connected appliances in real-time.

## Components

- **NodeMCU ESP8266**: Microcontroller used for WiFi communication.
- **Arduino IDE**: Software platform for writing, compiling, and uploading the code to the microcontroller.
- **Cloud Platform**: MQTT broker or other IoT cloud services to handle message publishing and subscribing.
- **Connected Devices**: Appliances or sensors connected to the NodeMCU ESP8266 for control and monitoring.

## Getting Started

### Prerequisites

- [Arduino IDE](https://www.arduino.cc/en/software)
- NodeMCU ESP8266 board
- An MQTT broker or IoT cloud platform (e.g., [Adafruit IO](https://io.adafruit.com/), [MQTT Dashboard](https://mqtt.eclipse.org/))

### Installation

1. **Set up Arduino IDE:**
   - Install the Arduino IDE from the [official website](https://www.arduino.cc/en/software).
   - Add the NodeMCU ESP8266 board to Arduino IDE via **File > Preferences** and add the following URL to the "Additional Board Manager URLs":
     ```
     http://arduino.esp8266.com/stable/package_esp8266com_index.json
     ```
   - Go to **Tools > Board > Board Manager**, search for "ESP8266," and install it.

2. **Install Required Libraries:**
   - Install the necessary libraries from the Library Manager (`Tools > Manage Libraries`) such as:
     - `PubSubClient` for MQTT communication.
     - `ESP8266WiFi` for WiFi connectivity.

### Usage

1. **Connect NodeMCU to PC**: Connect the NodeMCU ESP8266 to your computer via USB.
2. **Open the Project Code**: Open the `.ino` file in the Arduino IDE.
3. **Configure WiFi and MQTT Credentials**: Update the code with your WiFi SSID, password, and MQTT broker details.
4. **Upload the Code**: Select the correct board (NodeMCU 1.0) and port in the Arduino IDE, then click on the "Upload" button.
5. **Monitor the Serial Output**: Use the Serial Monitor in Arduino IDE to check the connection status and messages.

### Code Overview

- **Setup Function**: Initializes the WiFi connection and sets up MQTT communication.
- **Loop Function**: Handles MQTT message publishing and subscription, and controls devices based on received messages.
