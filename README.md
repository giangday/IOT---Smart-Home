# My Smart Home  

## Introduction  

**My Smart Home** is an **Internet of Things (IoT)** application project aimed at building a smart home system that allows users to remotely monitor and control household devices. This project focuses on **environmental monitoring**, **enhanced security**, and **energy efficiency** to improve quality of life. The system utilizes sensors to collect data on temperature, humidity, light, and gas or fire detection. This data is transmitted and processed, enabling users to monitor and control devices via a mobile application.  
![menu](https://github.com/giangday/IOT---Smart-Home/blob/main/Menu__.png?raw=true)
## Key Features  

- **Environmental Monitoring**:  
  - View real-time environmental parameters such as temperature, humidity, and light levels.  
  - Display environmental fluctuation charts over a specified period.  

- **Security Management**:  
  - Remotely monitor living areas through cameras.  
  - Receive alerts and danger notifications when incidents are detected.  

- **Remote Control**:  
  - Turn household appliances on/off remotely via the application.  
  - Automate device operations based on sensor thresholds.  
  - Schedule automatic device activation and deactivation.  

- **AI Integration**:  
  - Facial recognition for enhanced security.  
  - Voice recognition for device control.  

## System Architecture  

The **My Smart Home** system is built on four main functional components:  

1. **Things Layer**: Includes physical devices such as sensors, relays, and ESP32 microcontrollers.  
2. **IoT Gateway**: Acts as a bridge between devices and the server, utilizing the MQTT protocol for data transmission. The gateway is implemented using Python.  
3. **Server Layer**: Manages, stores, and processes data from devices while issuing control commands. Adafruit IO is used for data collection, processing, and visualization.  
4. **Application Layer**: Provides a user-friendly interface for monitoring and interacting with the system. The application is developed for Android platforms.  

## Technologies Used  

### Hardware  
- **ESP32** microcontroller  
- **DHT11** temperature and humidity sensor  
- Light sensor  
- **MQ2** gas sensor  
- Fire detection sensor  
- **LM2596** voltage regulator module  

### Software  
- **Python** (for IoT Gateway)  
  - **pyserial** library  
  - **Adafruit_IO** library  
  - **asyncio** library  
  - **threading** library  
- **Java** (for Android application)  
  - **Paho MQTT Android** library  
  - **org.eclipse.paho.client.mqttv3** library  
- **TensorFlow** (for facial recognition)  
- **Keras** (for facial recognition)  
- **OpenCV** (for facial recognition)  
- **NumPy** (for facial recognition)  
- **WebSockets** (for voice recognition)  

### Protocols  
- **UART** (communication between Things and Gateway)  
- **MQTT** (communication between Gateway, Server, and Application)  
