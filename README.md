# Meds_dispenserAtmega328P_1stProto
Smart Medicine Dispenser
Project Description
This automated medicine dispenser is designed to release medication at three scheduled times (morning, afternoon, and dinner) using stepper motors. The first prototype was built around an ATmega328P microcontroller (pulled from an Arduino UNO) and programmed using Atmel Studio 7.0 with an AVR 8051 USB ISP programmer.

Key Features
Time-Based Dispensing: Takes user input via Bluetooth (HC-05) to set the current time and three medication schedules.
Real-Time Tracking: Uses an RTC (DS3231) for accurate timekeeping.
Visual Feedback: Displays time and alerts on a 0.94" OLED screen.
Motor Control: Three 28BYJ-5V stepper motors (driven by ULN2003) rotate 45° to dispense pills when scheduled.
Power Management: A 12V input is stepped down to 5V using an AMS1117 regulator for safe operation.

How It Works
User Input Setup
The user sets the current time and three medication times via Bluetooth (HC-05).
The RTC (DS3231) is updated, and the schedule is displayed on the OLED for verification.

Automated Dispensing
The system continuously checks the RTC.
When the current time matches a scheduled time, the corresponding stepper motor rotates 45°, dispensing the medicine.
A confirmation message (e.g., "Afternoon medicine dispensed") appears on the OLED.

Daily Reset
The system loops indefinitely, dispensing medication at the same times every day.

Hardware Components
ATmega328P (from Arduino UNO) -> Main microcontroller (11.0592 MHz oscillator)
HC-05 Bluetooth Module ->	Wireless input for time settings
DS3231 RTC	-> Keeps accurate time for scheduling
0.94" OLED Display	-> Shows time, settings, and dispensing alerts
28BYJ-5V Stepper Motors (x3)	-> Rotate to dispense pills
ULN2003 Motor Drivers (x3)	-> Control stepper motors
AMS1117 5V Regulator ->	Converts 12V input to 5V for components
Rocker Switch ->	Power control

-I've also attached the schematics and pcbs(2 layers) design in kicad along with a video of testing components pls feel free to refer those.
