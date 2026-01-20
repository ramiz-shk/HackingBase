\# 🔐 Wireless Solenoid Lock System using Arduino + NRF24L01 + RFID



This project is a simple, reliable \*\*wireless lock system\*\* built using two Arduino boards (Uno/Nano), \*\*NRF24L01\*\* wireless modules, an \*\*RFID card reader\*\*, a \*\*12V solenoid lock\*\*, a \*\*relay\*\*, and a \*\*push button\*\*. You can unlock the solenoid using either an \*\*RFID card\*\* or a \*\*remote push button\*\*.



---



\## 🧠 Features



\- Dual-mode unlocking: RFID card + wireless remote

\- Wireless communication using NRF24L01

\- Solenoid lock controlled by relay module

\- Portable design powered by 7.4V or 11.1V battery pack

\- Secure and reliable multi-authentication

\- Ideal for smart lockers, cabinets, or custom entry systems



---



\## 📦 Components Required



| Component              | Quantity  |

| ---------------------- | --------- |

| Arduino Uno / Nano     | 2         |

| NRF24L01 Module        | 2         |

| MFRC522 RFID Reader    | 1         |

| RFID Card/Tag          | 1         |

| Relay Module (5V)      | 1         |

| 12V Solenoid Lock      | 1         |

| Push Button            | 1         |

| 3.7V Li-ion Cells      | 2 or 3    |

| AMS1117 3.3V Regulator | 1         |

| 470µF Capacitor        | 1         |

| Battery Holder/Pack    | 1         |

| Jumper Wires           | as needed |



---



\## 🔌 Connections



\### 📡 NRF24L01 to Arduino (Both Transmitter \& Receiver)



| NRF24L01 | Arduino                                    |

| -------- | ------------------------------------------ |

| GND      | GND                                        |

| VCC      | 3.3V ⚠️ (from AMS1117 or regulated source) |

| CE       | D9                                         |

| CSN      | D10                                        |

| SCK      | D13                                        |

| MOSI     | D11                                        |

| MISO     | D12                                        |



> 💡 Add a \*\*470µF capacitor\*\* across VCC and GND near the NRF24L01 module for stability.



---



\### 🟢 Transmitter (Arduino Uno)



\- Push Button → D2

\- Powered via USB or 7.4V Battery → VIN



---



\### 🔴 Receiver (Arduino Nano)



\- \*\*Relay IN\*\* → D4

\- \*\*Relay COM\*\* → 12V Battery +

\- \*\*Relay NO\*\* → Solenoid +

\- \*\*Solenoid –\*\* → 12V Battery GND



\#### RFID (MFRC522)



| RFID Pin | Arduino Nano |

| -------- | ------------ |

| SDA      | D6           |

| RST      | D5           |

| MOSI     | D11          |

| MISO     | D12          |

| SCK      | D13          |

| VCC      | 3.3V ⚠️      |

| GND      | GND          |



\- Arduino powered via \*\*VIN\*\* from 7.4V/11.1V battery



---



\## 💾 Code



\- 🔗 \*\*Transmitter Code\*\*: `transmitter.ino`  

&nbsp; Sends `"UNLOCK"` signal wirelessly on button press.



\- 🔗 \*\*Receiver Code\*\*: `receiver.ino`  

&nbsp; Listens for:

&nbsp; - `"UNLOCK"` signal via NRF → triggers relay for 3 sec

&nbsp; - or valid RFID UID → triggers relay for 3 sec



---



\## 🔋 Power Notes



\- Use \*\*7.4V or 11.1V battery\*\* to power system via VIN pin

\- Battery should supply \*\*at least 2A\*\* during solenoid activation

\- Power NRF24L01 via \*\*AMS1117 3.3V\*\* with a 470µF capacitor

\- Relay safely isolates solenoid from Arduino



---



\## ✅ To-Do / Ideas



\- Add toggle mode: press once = unlock, press again = lock

\- Add keypad for multi-authentication

\- Use sleep mode for low-power standby

\- Add OLED display for UID logs or status



