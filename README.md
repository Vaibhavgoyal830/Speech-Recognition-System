# Speech-Recognition-System
✅ Project: Basic Speech Recognition System for Command-Based Control of Devices
🎯 Objective:
To build a system that listens to voice commands (like “Turn on light”, “Turn off fan”) and controls devices using an embedded board (like Arduino or ESP32) and a speech recognition module.

🔧 System Design
🧰 Required Components:
Component	Quantity
Arduino Uno / Nano / ESP32	1
Voice Recognition Module V3 (Elechouse)	1
Relay Module (2-channel or 4-channel)	1
Loads (Bulb, Fan, etc. or use LEDs)	2
Jumper Wires & Breadboard	—
External 5V Power Supply	1

🔌 Block Diagram:
csharp
Copy
Edit
[Microphone Input]
       ↓
[Voice Recognition Module]
       ↓
[Arduino / ESP32]
       ↓
[Relay Module]
       ↓
[AC Devices (Light, Fan)]
🧾 How It Works:
You train the voice module with a set of specific commands like:

"Light On"

"Light Off"

"Fan On"

"Fan Off"

The module listens to voice inputs.

On matching a command, it sends a serial code to the Arduino.

Arduino reads the command and toggles the appropriate relay.

📟 Connections:
Voice Module TX → Arduino RX

Voice Module RX → Arduino TX

Relay IN1 → Arduino D8

Relay IN2 → Arduino D9

Relay → Connected to AC loads or LEDs

Module/Relay Power → 5V from Arduino or separate supply

The actual character ('A', 'B', etc.) depends on how the Voice Recognition Module was trained and configured.

🗣️ Training Voice Commands (for Elechouse V3):
You can use the included serial PC tool to:

Record up to 80 voice commands

Assign a number or code to each

Group them for use (e.g., Group 1 for Lights, Group 2 for Fan)

✅ Deliverables Checklist:
Item	Status
✅ System Design Diagram	✅ Done
✅ Arduino Code	✅ Done
✅ Working Demonstration	(Use LEDs or real devices)
✅ Speech Recognition Trained Commands	(via PC Tool)
