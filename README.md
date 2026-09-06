

# Voice-Controlled RC Car

An embedded systems project featuring a voice-controlled robotic vehicle powered by an ATmega328P microcontroller (Arduino) and an H-Bridge motor driver. Commands are transmitted wirelessly via Bluetooth from a smartphone voice application.

## Key Features
* **Voice Command Navigation:** Real-time execution of commands (`forward`, `backward`, `left`, `right`, `stop`).
* **H-Bridge Differential Drive:** Uses L298N driver for bidirectional control and PWM speed adjustment.
* **Software Serial Communication:** Custom serial interface handling UART data streams at 9600 baud.
* **Failsafe System:** Auto-stops motors if an unknown command or communication loss occurs.

## Hardware Circuit Connections

| Component | Component Pin | Arduino UNO Pin |
| :--- | :--- | :--- |
| **HC-05 Bluetooth** | TX | Pin 2 (Soft RX) |
| | RX | Pin 3 (Soft TX) |
| | VCC / GND | 5V / GND |
| **L298N Driver** | ENA (Speed L) | Pin 5 (PWM) |
| | IN1 / IN2 | Pin 6 / Pin 7 |
| | IN3 / IN4 | Pin 8 / Pin 9 |
| | ENB (Speed R) | Pin 10 (PWM) |
| | GND | Common GND |

## System Logic Architecture
