🤖 Light-Following Robot with Bluetooth Control and Safety Features

This project showcases a multifunctional autonomous robot designed using Arduino Uno, capable of tracking light, avoiding it on command, handling no-light situations with a buzzer warning, and accepting manual control via Bluetooth. The system is built for educational purposes and demonstrates sensor-based navigation, wireless communication, and safety integration.

🎯 Project Objectives

Build a robot that follows light using LDRs (Light Dependent Resistors).

Allow the user to switch to light-avoidance mode using a button.

Provide visual feedback through LEDs (Green = Follow, Red = Avoid).

Trigger a buzzer and shut down if no light is detected for 40 seconds.

Enable full manual control via Bluetooth through a smartphone.

Combine all behaviors into one seamless autonomous/manual system.

🛠️ Core Functionalities

✅ 1. Light-Following Mode (default)

Robot moves toward light detected by LDR sensors.

Uses analog light intensity readings to decide direction (left/right/forward).

✅ 2. Light-Avoiding Mode (toggled via button)

When the button is pressed, the robot reverses logic and moves away from light.

Toggled LED feedback: Green = follow, Red = avoid.

✅ 3. No Light Detected

If both LDRs detect no significant light for 40 seconds:

Robot stops moving

Buzzer sounds for 2 seconds

System goes into shutdown mode until reset

✅ 4. Bluetooth Manual Control

Connect your smartphone to the HC-06 Bluetooth module.

Send single-character commands via a Bluetooth terminal app:

F = Move Forward

B = Move Backward

L = Turn Left

R = Turn Right

S = Stop

D = Dance (demo mode with blinking lights and movement)

⚙️ Components Used

Component

Purpose

Arduino Uno

Central control unit

4x DC Motors + Wheels

Movement

L298N Motor Driver

Drives motors

2x LDR Sensors

Light detection

HC-06 Bluetooth Module

Wireless manual control

Push Button

Toggle between follow/avoid modes

2x LEDs (Red, Green)

Mode indicators

Buzzer

Warning on no light detection

12V Battery + Holder

Power supply

Jumper Wires & Breadboard

Connections and prototyping

Ultrasonic Sensor

(Optional) rear obstacle detection

💡 Technical Notes

Sensors were covered with custom dark paper hoods to reduce ambient light interference and narrow detection range.

The LDR threshold for “no light” was experimentally set to 600 (analog value).

analogWrite() used to control motor speeds via enable pins.

