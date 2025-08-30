# IoT-Power-Consumption-WSN-Optimization

This project explores the design and analysis of an IoT-based parking occupancy detection system using an ESP32 microcontroller, an ultrasonic sensor, and esp_now Wi-Fi communication. The study also evaluates energy consumption patterns across different operating states (transmission, deep sleep, and sensor read), and investigates sink node optimization in a Wireless Sensor Network (WSN) to maximize system lifetime.
Project Overview

1.	Parking Occupancy Node
-	Implemented in Wokwi using ESP32 + HC-SR04 ultrasonic sensor.
-	Detects whether a parking space is free or occupied.
-	Sends messages via esp_now protocol ("Free" or "Occupied").
-	Utilizes deep sleep to reduce power consumption.

2.	Energy Consumption Estimation
-	Analyzed real power consumption data from three scenarios:
	Transmission Power (low/high states, idle state)
	Deep Sleep Cycles (Wi-Fi on/off, sleep mode)
	Sensor Reading (active vs. idle phases)
-	Data processed using Python (CSV parsing, timestamp handling, histograms).
-	Calculated average power, energy per cycle, and battery lifetime.
-	Battery capacity used: 16,128 J.

3.	Optimization & Improvements
-	Proposed adaptive sensing to reduce redundant transmissions.
-	Suggested batch data transmission for efficiency.
-	Highlighted potential gains in battery life and system reliability.

4.	Wireless Sensor Network (WSN) Sink Optimization
-	Evaluated system lifetime based on sensor-to-sink distances.
-	Found optimal sink position ≈ [6.9 , 7.6].
-	Discussed trade-offs:
	Fixed sink → simpler, lower cost, but reduced lifetime.
	Mobile sink → extended lifetime, balanced energy use, but higher complexity.

