# Advanced Python Network Sniffer 🛰️

## Overview
A lightweight, high-performance network analysis tool engineered in Python using the **Scapy** library. This tool intercepts live network packets traversing the local interface, providing real-time visibility into source/destination communication and transport layer protocols.

## Key Features
- **Live Packet Interception:** Captures raw IPv4 traffic directly from the network interface.
- **Protocol Identification:** Automatically categorizes traffic into TCP, UDP, or other protocol types.
- **Real-time Parsing:** Extracts and displays source and destination IP addresses for every packet.
- **Security Analysis:** Useful for identifying unauthorized network connections or analyzing DNS/Web traffic patterns.

## Skills Demonstrated
- **Socket Programming:** Understanding how data travels across the OSI model (Layer 3 & 4).
- **Traffic Analysis:** Hands-on experience with packet structure and protocol handshakes.
- **Linux Security:** Managing elevated permissions (sudo/root) to access raw network sockets in Kali Linux.

## Tools & Environment
- **Language:** Python 3
- **Library:** Scapy
- **Platform:** Kali Linux (VirtualBox)

## How to Run
1. Ensure Scapy is installed: `sudo apt install python3-scapy`
2. Run the script with root privileges: `sudo python3 my_sniffer.py`
3. Generate traffic by opening a web browser and observe the live capture in the terminal.
