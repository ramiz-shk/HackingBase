\# 🔒 Smart Door Lock System

\*\*Created by:\*\* Ramiz | \*\*Tech:\*\* Arduino, RFID, C++



\## 📖 Overview

This is a secure, contactless door entry system designed for home automation. It uses \*\*RFID technology\*\* to grant access only to authorized cards. It features a wireless control unit for remote unlocking.



\## 🛠️ Hardware Used

\- \*\*Microcontroller:\*\* Arduino / ESP32

\- \*\*Sensor:\*\* MFRC522 RFID Module

\- \*\*Actuator:\*\* Solenoid Lock 12V

\- \*\*Power:\*\* 12V 2A Adapter



\## ⚙️ How it Works

1\. User scans the RFID tag.

2\. System checks the UID against the database.

3\. If authorized -> \*\*Green LED\*\* turns on \& Lock opens.

4\. If unauthorized -> \*\*Red LED\*\* blinks \& Access Denied.



\## 📸 Photos

!\[Circuit Diagram](circuit.jpg)

\*(Note: You need to add an image named circuit.jpg to your folder for this to work)\*



\## 🚀 Future Improvements

\- \[ ] Add Fingerprint sensor

\- \[ ] Connect to WiFi for Phone App Control

