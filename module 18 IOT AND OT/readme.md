
Module 18: IoT & OT Hacking
1. Introduction to IoT

IoT = network of interconnected smart devices that communicate autonomously.

Components:

Sensors / Actuators

Connectivity layer (Wi-Fi, ZigBee, BLE, LoRa)

Cloud / Edge processing

User interface / APIs

Real-world uses: smart homes, healthcare devices, CCTV, wearables, industrial sensors.

2. IoT Ecosystem & Architecture

Perception Layer: sensors, RFID, microcontrollers

Network Layer: routing, switching, wireless protocols

Application Layer: cloud apps, dashboards, APIs

IoT often lacks strong updates, encryption, and authentication.

3. IoT Attack Surface

Hardware: UART/JTAG pins, memory chips

Firmware: backdoors, insecure coding

Communication protocols: MQTT, CoAP, BLE, Zigbee

Mobile apps: reverse engineering APKs

Cloud & API endpoints

Default passwords and weak authentication

4. Common IoT Vulnerabilities

Hardcoded credentials

Unencrypted communication

Insecure web interfaces

Outdated firmware

Exposed ports (HTTP, Telnet, SSH)

Weak OTA update mechanism

Device misconfiguration

Insecure APIs

5. IoT Hacking Methodology
Reconnaissance

Identify device, OS, firmware, services

Tools: Shodan, Nmap, Censys, Fing

Vulnerability Analysis

Firmware extraction

Analyze services, weak protocols

Tools: Binwalk, Ghidra, MobSF, Nmap scripts

Exploitation

Bypass login

Default-password attack

Binwalk-based firmware exploit

Command injection

MITM via Wi-Fi/Bluetooth sniffing

Post-Exploitation

Maintain persistence

Pivot inside internal network

Create IoT botnet (Mirai-like)

6. IoT Hacking Tools (as listed in GitHub PDF reports)

Shodan – discover exposed IoT devices

Binwalk – firmware extraction

Firmware Mod Kit

Wireshark

Bettercap – MITM

Nmap NSE Scripts (iot-vuln)

Ghidra / IDA Pro – reverse engineering

RFCrack – RF hacking

Kismet – Wi-Fi/BLE sniffing

7. Introduction to OT (Operational Technology)

OT controls industrial environments like:

Power grids

SCADA

Water plants

PLCs/RTUs

OT focuses on availability + safety, not confidentiality.

8. OT Protocols

Modbus

DNP3

OPC-UA

BACnet

Profibus / PROFINET

These protocols often lack encryption and authentication.

9. OT Threats & Attacks

Unauthorized PLC access

Manipulation of industrial processes

Man-in-the-middle attacks

Firmware tampering

ICS malware

Real-world attacks:

Stuxnet

Triton

BlackEnergy

Industroyer

10. IoT & OT Security Countermeasures

Change all default passwords

Secure firmware updates

Edge-device hardening

Use encrypted protocols

API rate-limiting + access control

Network segmentation (IT vs OT)

Continuous monitoring (SIEM)

Patch management

Disable unused services
