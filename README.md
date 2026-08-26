Battery Guard AI 🔋🤖
Introduction

Battery Guard AI is an intelligent battery monitoring and safety system designed to monitor the condition and performance of a 12 V battery in real time. The project combines IoT sensors, an ESP32 microcontroller, Wi-Fi communication, and AI-based analysis to provide useful information about battery health and potential safety risks.

The system uses an INA219 sensor to measure voltage, current, and power consumption. A DS18B20 sensor monitors the temperature of the battery surface, while a DHT11 sensor measures ambient temperature and humidity. The collected sensor data is displayed locally on an LCD and transmitted through Wi-Fi for monitoring on a dashboard.

The project aims to estimate the battery's State of Health (SoH), calculate a safety risk level, predict possible degradation, and provide recommendations based on the monitored conditions.

Working

The 12 V battery is connected to a load through a fuse and the INA219 current sensor. The INA219 measures the battery voltage and current flowing to the load, while the ESP32 calculates the power consumption.

The DS18B20 sensor is attached to the battery surface to continuously monitor battery temperature. The DHT11 sensor measures the surrounding temperature and humidity.

All sensor readings are collected by the ESP32. The ESP32 processes the data and displays important values such as voltage, current, power, temperature, risk level, and estimated State of Health on the 16×2 LCD.

Using its built-in Wi-Fi, the ESP32 sends the sensor data to a laptop, server, or web dashboard. The dashboard displays live values, historical graphs, battery status, and AI predictions.

The system analyzes parameters such as voltage, current, power, and temperature to determine the battery condition. Based on these values, the battery is classified into three states:

Normal – Battery operating within expected conditions.
Warning – Abnormal changes in voltage, current, or temperature are detected.
High Risk – Significant battery stress or potentially unsafe conditions are detected.

The AI analysis provides an estimated State of Health (SoH), Safety Risk Score, and Degradation Forecast. It can also generate an explanation showing which factors, such as increasing temperature or abnormal current, are contributing to the increased risk.
