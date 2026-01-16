# TryHackMe – Cyber Security 101

This repository documents my hands-on learning from the **TryHackMe Cyber Security 101 path**.

All rooms included here have been **personally completed by me** and are documented honestly for learning and portfolio purposes.

---

## 👨‍💻 About Me
I am a motivated Cyber Security student actively building hands-on skills through structured labs on TryHackMe. My focus is on developing a strong foundation in command-line operations, networking fundamentals, and security concepts relevant to SOC (Security Operations Center) roles. I document only the labs I have personally completed to maintain accuracy and credibility in my learning journey.

---

## 📚 Completed Sections

### 🔹 Start Your Cyber Security Journey
- Offensive Security Intro
- Defensive Security Intro
- Search Skills

### 🔹 Linux Fundamentals
- Linux Fundamentals Part 1
- Linux Fundamentals Part 2
- Linux Fundamentals Part 3

### 🔹 Windows & Active Directory Fundamentals
- Windows Fundamentals Part 1
- Windows Fundamentals Part 2
- Windows Fundamentals Part 3
- Active Directory Basics

### 🔹 Command Line
- Windows Command Line
- Windows PowerShell
- Linux Shells
- Shell Scripting & Components

- ### ### 🔹 Networking Fundamentals

- **Networking Concepts**  
  Learned core networking principles including networks, devices, and data communication basics.

- **Networking Core Protocols**  
  Studied key protocols such as TCP, UDP, and IP and their role in data transmission.

- **Networking Essentials**  
  Covered practical networking essentials such as addressing, traffic flow, and network components.

- **Networking Secure Protocols**  
  Explored secure networking protocols and how encryption protects data in transit.

  ### 🔹 Traffic Analysis & Packet Inspection

- **Wireshark: The Basics**  
  Hands-on introduction to packet capture and network traffic analysis using Wireshark.

- **TCPDUMP: The Basics**  
  Learned command-line packet capture and traffic analysis using tcpdump.  

  ### 🔹 Network Reconnaissance

- **Nmap: The Basics**  
  Learned basic network scanning and service discovery using Nmap.

📌 Wireshark Live Traffic Analysis (Hands-On Lab)
🔹 Lab Type
Real-World Practice (Local Machine)
🔹 Tools Used
Wireshark
Windows 11
🔹 Objective
To capture and analyze live network traffic using Wireshark and understand how common protocols behave in real-time, focusing on skills required for a SOC Level 1 Analyst role.
🔹 Lab Activities Performed
Captured live network traffic using an active network interface
Identified common network protocols such as:
TCP
UDP
DNS
TLS
Applied display filters to isolate specific traffic (e.g., DNS, TCP)
Analyzed HTTPS traffic using port 443
Followed a TCP stream to understand session communication
Observed DNS queries and responses
Reviewed packet details including:
Source and destination IP addresses
Ports
Flags (SYN, ACK, FIN)
🔹 Key SOC Skills Practiced
Network traffic monitoring
Packet inspection and protocol identification
Understanding encrypted traffic (HTTPS/TLS)
Detecting normal network behavior
Using Wireshark for incident investigation support
🔹 Outcome
This lab improved my practical understanding of live network traffic analysis and strengthened core skills required for SOC Level 1 / Cyber Security Intern positions.
🔹 Evidence
Live traffic captured using Wireshark
Packet analysis performed in real time
Screenshots and .pcapng file stored locally   

## 🔬 Lab 1: HTTP vs HTTPS Traffic Analysis (Wireshark)

### 🎯 Objective
To analyze live network traffic and understand the difference between HTTP and HTTPS communication using Wireshark.

---

### 🛠 Tools Used
- Wireshark
- Windows 11
- Wi-Fi Network

---

### 🧪 Lab Tasks Performed
- Captured live network traffic
- Identified HTTP traffic on port 80
- Identified HTTPS traffic on port 443
- Compared readable vs encrypted traffic
- Saved capture file for analysis

---

### 🔍 Key Observations

**HTTP (Port 80):**
- Traffic is sent in plain text
- URLs, headers, and requests are readable
- Not secure

**HTTPS (Port 443):**
- Traffic is encrypted using TLS
- Packet content is not readable
- Secure communication

---

### 📸 Screenshots
| Description | Evidence |
|------------|----------|

| HTTP Traffic | <img width="1920" height="1200" alt="Screenshot 2026-01-16 004026" src="https://github.com/user-attachments/assets/0eb4661e-1883-4ab6-adbe-11b2efd74711" />

| HTTPS Traffic | <img width="1920" height="1200" alt="Screenshot 2026-01-16 004514" src="https://github.com/user-attachments/assets/7edcf618-e310-47ef-b3c7-4625de4cafe5" />

## 🧪 Wireshark Lab 2 – DNS Traffic Analysis

### 🎯 Objective
Capture and analyze DNS traffic using Wireshark to identify domain names, record types, and determine whether the traffic is normal or suspicious.

---

### 🛠 Tools Used
- Wireshark
- Windows 11
- Wi-Fi Network Interface

---

### 🔍 Lab Steps
1. Started live capture on the Wi-Fi interface
2. Applied display filter:

3. 3. Observed DNS query and response packets
4. Analyzed domain name and DNS record type

---

### 🌐 Analysis Results
- **Domain Name:** `wpad.communityfibre.co.uk`
- **DNS Record Type:** `A`
- **Protocol:** DNS
- **Port:** 53
- **Traffic Verdict:** Normal / Non-suspicious

---

### 📸 Evidence
- <img width="1920" height="1200" alt="Screenshot 2026-01-16 010120" src="https://github.com/user-attachments/assets/37ef6978-a43f-49d0-9bbb-a0f9176f1c4b" />


---

### 🧠 SOC Analyst Notes
- DNS typically uses UDP port 53
- Normal DNS traffic is common in daily network activity
- No suspicious indicators observed in this lab




---

### 🧠 SOC Relevance
- Helps identify insecure traffic
- Useful for detecting data exposure risks
- Fundamental skill for SOC Level 1 Analysts


# Lab 3 – TCP 3-Way Handshake Analysis (Wireshark)

## Objective
To analyze and understand the TCP 3-way handshake process using Wireshark and identify TCP flags involved in establishing a connection.

## Environment
- OS: Windows 11  
- Tool: Wireshark  
- Network: Wi-Fi  
- Capture Type: Live traffic  

## What I Did
1. Started live packet capture on the Wi-Fi interface.
2. Applied display filter to focus on TCP traffic.
3. Identified TCP packets involved in a connection setup.
4. Analyzed TCP flags to confirm the 3-way handshake process.
5. Captured and saved evidence for documentation.

## Key Findings
- **SYN** flag: Client initiating connection.
- **SYN, ACK** flags: Server acknowledging and responding.
- **ACK** flag: Client confirming connection establishment.
- Protocol used: **TCP**
- Connection established successfully with no anomalies detected.

## SOC Relevance
Understanding TCP handshakes is essential for:
- Detecting abnormal connection attempts
- Identifying SYN floods or scanning activity
- Validating legitimate vs malicious network traffic

## Evidence
- Packet Capture File: `lab3-tcp-3way-handshake.pcapng`
- Screenshot:
- <img width="1920" height="1200" alt="Screenshot 2026-01-16 011420" src="https://github.com/user-attachments/assets/8f854128-6254-44bb-b9ef-c73bbd5a0537" />



  
  
  

---

## 🎯 Goal
To continue progressing towards **SOC Level 1** with a focus on defensive security and monitoring.
