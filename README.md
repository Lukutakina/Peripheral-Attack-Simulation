# Peripheral Attack Simulation Group 22

Adrian Ståhlberg  
Felix Jondelius  
Wilma Winther  

## Project Overview

This project demonstrates a USB peripheral attack simulation using a Raspberry Pi Pico 2W configured as a Human Interface Device  
When connected to a target system the device automatically executes predefined keystrokes to open a web browser display security information and show non sensitive system information  

This project is strictly non malicious and intended for educational and research purposes only  
The goal is to illustrate how real world USB attacks could function if used maliciously  

This project was developed as part of a university course at Halmstad University Sweden and is intended solely for academic use and learning  

## Purpose

The purpose of this project is to demonstrate how a USB peripheral can execute commands automatically when inserted  
It aims to highlight the risks of BadUSB and HID keyboard injection attacks  
It also increases awareness of human factor vulnerabilities in cybersecurity  
The project provides a safe and controlled simulation environment for learning and analysis  

## Threat Model

Attack type BadUSB HID keyboard injection  
Attack vector USB peripheral acting as a keyboard  
Target operating system Windows 10  
Payload type benign command execution  
Persistence none  
Data sensitivity non sensitive system metadata only  

No malware persistence mechanisms or data exfiltration are used  

## Hardware and Software Requirements

### Hardware

Raspberry Pi Pico 2W  
USB cable  
Test computer or Windows 10 virtual machine  

### Software

CircuitPython firmware  
Adafruit CircuitPython HID library  
Thonny IDE  
English US keyboard layout  
Windows 10  

## Repository Structure

README md  
payloads folder containing benign ducky script text file  
prompts folder containing llm usb prompts text file  

## Folder Descriptions

payloads contains documentation of intended keystroke logic and bootfile
prompts contains AI prompts used to generate initial code  

## Setup Instructions Summary

Flash CircuitPython firmware to the Raspberry Pi Pico  
Copy the adafruit hid library into the lib directory  
Place boot py and code py onto the device  
After setup the device will execute automatically when inserted  

Testing should only be performed in a controlled environment  

## Safety and Ethical Considerations

The project uses benign commands only  
No persistence malware or sensitive data access is implemented  
Testing was conducted only in a controlled virtual machine environment  
The project follows academic ethical guidelines  

This simulation must never be used on unauthorized systems  

## Limitations

The device does not physically resemble a real USB stick due to budget constraints  
Operating system detection is not implemented and Windows is assumed  
HID timing may vary between systems  
Detection evasion techniques are intentionally excluded  

## Prevention and Mitigation Summary

This project highlights the importance of USB device control and whitelisting  
Disabling unnecessary USB classes  
Firmware integrity validation  
Operating system hardening  
User education which remains the most critical defense  

## License

This project is released under the MIT License  
See the LICENSE file in this repository for full license text  

## Disclaimer

This project is for educational purposes only  
The authors assume no responsibility for misuse of the techniques demonstrated  
