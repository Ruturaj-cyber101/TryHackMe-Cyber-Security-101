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


# Lab 4 – ICMP / Ping Traffic Analysis (Wireshark)

## Objective
To analyze ICMP (Internet Control Message Protocol) traffic using Wireshark and understand how ping (Echo Request and Echo Reply) works from a SOC Level 1 perspective.

## Environment
- OS: Windows 11  
- Tool: Wireshark  
- Network Interface: Wi-Fi  
- Capture Type: Live traffic  
- Command Used: ping 8.8.8.8  

## Lab Setup
1. Opened Wireshark and selected the Wi-Fi interface.
2. Started live packet capture.
3. Generated ICMP traffic using Command Prompt.
4. Applied ICMP filter to analyze packets.
5. Saved packet capture and collected evidence.

## Steps Performed
1. Started Wireshark capture on Wi-Fi interface.
2. Opened Command Prompt and ran:
3. Stopped ping after a few seconds.
4. Applied display filter:
5. Selected ICMP packets and analyzed protocol details.
6. Stopped capture and saved the file.

## Analysis & Findings
- ICMP Echo Request:
- Type: 8
- Sent by client to check host availability.
- ICMP Echo Reply:
- Type: 0
- Sent by destination host as a response.
- ICMP does not use TCP or UDP.
- ICMP works at the Network Layer (Layer 3).
- No ports or TCP flags are used.

## SOC Relevance
ICMP analysis helps SOC analysts to:
- Identify network connectivity checks
- Detect ICMP floods or scanning activity
- Distinguish normal ping traffic from malicious behavior

## Conclusion
The observed ICMP traffic represents normal ping activity. There were no signs of suspicious or malicious behavior in this capture.

## Evidence
- Packet Capture: `lab4-icmp-ping-analysis.pcapng`
<img width="1920" height="1200" alt="Screenshot 2026-01-18 032534" src="https://github.com/user-attachments/assets/207cee37-9c37-443a-a540-c6ba41aeb1cc" />

  

## Status
✅ Lab completed successfully
  
 # 🧪 Wireshark Lab 5 – ARP Traffic Analysis

## 🎯 Lab Objective
To understand how ARP (Address Resolution Protocol) works, identify ARP requests, replies, and announcements, and analyze whether the traffic is normal or suspicious from a SOC Level 1 perspective.

---

## 🛠 Tools Used
- Operating System: Windows 11
- Tool: Wireshark
- Network Interface: Wi-Fi

---

## 📌 Lab Setup
- Wireshark installed and running
- Active internet connection
- Packet capture started on Wi-Fi interface
- Display filter used:
```plaintext
arp
```

---

## 🧾 Lab Tasks Performed
1. Started packet capture on Wi-Fi interface
2. Applied ARP display filter
3. Observed ARP requests, replies, and announcements
4. Selected an ARP packet for detailed analysis
5. Captured screenshot for documentation
6. Saved capture file
7. Updated GitHub repository

---

## 🔍 Observations & Analysis

### 1️⃣ ARP Request
Observed multiple ARP requests such as:
```plaintext
Who has 192.168.1.74? Tell 192.168.1.74
```

This indicates a **Gratuitous ARP / ARP Announcement**, where a device announces its own IP address to the network.

---

### 2️⃣ ARP Packet Details
From the selected packet:
```plaintext
Sender IP Address: 192.168.1.74
Sender MAC Address: 80:c0:1e:12:24:2e
Target IP Address: 192.168.1.74
Target MAC Address: 00:00:00:00:00:00
Destination MAC: ff:ff:ff:ff:ff:ff
Opcode: Request (1)
```

This confirms it is an **ARP Announcement** and not an attack.

---

### 3️⃣ ARP Reply
Observed ARP replies such as:
```plaintext
192.168.1.1 is at 80:69:1a:xx:xx:xx
```

This shows successful IP-to-MAC resolution on the local network.

---

### 4️⃣ Protocol Characteristics
- Protocol: ARP
- OSI Layer: Layer 2 (Data Link)
- Transport Layer: Not applicable (No TCP/UDP)
- Packet Length: 42 bytes
- Communication Type: Broadcast (Request), Unicast (Reply)

---

### 5️⃣ Traffic Assessment
- No duplicate IP addresses detected
- No conflicting MAC addresses
- No ARP flooding observed
- No unsolicited ARP replies

✅ Traffic behavior is **normal**.

---

## 🛡 SOC Level 1 Relevance
From a SOC analyst perspective, ARP analysis is used to detect:
- ARP Spoofing
- Man-in-the-Middle (MITM) attacks
- Rogue devices on the local network

In this lab:
- No Indicators of Compromise (IOCs) were found
- ARP activity matches normal baseline behavior

---

## 📸 Evidence
- One screenshot captured showing ARP packet details
  <img width="1920" height="1200" alt="Screenshot 2026-01-18 034341" src="https://github.com/user-attachments/assets/03d7902d-3bca-4948-b046-e2568ee32ca5" />


---

## 📁 Artifacts Saved
- Wireshark capture file (.pcapng)
- Screenshot (.png)

---

## ✅ Lab Status
**Completed**


# Lab 6 – DHCP Traffic Analysis using Wireshark

## 🎯 Objective
To analyze DHCP (Dynamic Host Configuration Protocol) traffic using Wireshark and understand how IP addresses are assigned to clients. This lab focuses on identifying DHCP Discover, Offer, Request, and ACK messages from a SOC Level 1 perspective.

---

## 🛠 Tools Used
- Operating System: Windows 11
- Tool: Wireshark
- Network Interface: Wi-Fi

---

## 📌 Lab Setup
- Wireshark installed and running
- Active network connection
- Packet capture started on Wi-Fi interface
- Display filter used:
```plaintext
dhcp
```
(or)
```plaintext
bootp
```

---

## 🧾 Lab Tasks Performed
1. Started live packet capture on Wi-Fi interface
2. Generated DHCP traffic using Command Prompt
3. Applied DHCP display filter
4. Observed DHCP Discover, Offer, Request, and ACK packets
5. Analyzed DHCP fields and server information
6. Captured screenshot for evidence
7. Saved packet capture file
8. Updated GitHub documentation

---

## 🔍 Observations & Analysis

### 1️⃣ DHCP Discover
- Message Type: DHCP Discover
- Wireshark Label: BOOTREQUEST
- Source IP: 0.0.0.0
- Destination IP: 255.255.255.255

This message is sent by the client to locate available DHCP servers on the network.

---

### 2️⃣ DHCP Offer
- Offered IP Address: 192.168.1.X
- DHCP Server IP: 192.168.1.1

The DHCP server responds with an available IP address for the client.

---

### 3️⃣ DHCP Request
The client requests the offered IP address from the DHCP server to confirm assignment.

---

### 4️⃣ DHCP ACK
The DHCP server acknowledges the request and finalizes the IP assignment.

---

### 5️⃣ Protocol Characteristics
- Protocol: DHCP
- Transport Layer: UDP
- Client Port: 68
- Server Port: 67
- OSI Layer: Application Layer

---

### 6️⃣ Traffic Assessment
- Single DHCP server observed
- No multiple offers detected
- No abnormal IP ranges
- No rogue DHCP behavior

✅ Traffic behavior is **normal**.

---

## 🛡 SOC Level 1 Relevance
SOC analysts monitor DHCP traffic to:
- Detect rogue DHCP servers
- Identify MITM preparation attacks
- Detect abnormal IP assignments
- Investigate internal network issues

No indicators of compromise were identified in this capture.

---

## 📸 Evidence
- Screenshot showing DHCP Discover, Offer, and ACK packets
- <img width="1920" height="1200" alt="Screenshot 2026-01-18 040511" src="https://github.com/user-attachments/assets/baef66bb-3e08-4a07-9e25-edf21a54a6c1" />


---

## 📁 Artifacts Saved
- lab6-dhcp-traffic-analysis.pcapng
- DHCP analysis screenshot (.png)

---

## ✅ Lab Status
**Completed**

---

## 🧠 Key Takeaways
- DHCP automates IP address assignment
- DHCP uses UDP ports 67 and 68
- Monitoring DHCP is critical for detecting internal network threats
- Wireshark is effective for DHCP traffic analysis

---

## 🧠 Key Learning
- ARP maps IP addresses to MAC addresses
- Gratuitous ARP is normal behavior
- SOC analysts monitor ARP to detect local network attacks
- Wireshark is effective for Layer 2 traffic analysis 

  ## 🧪 Lab 7 – TCP SYN / Port Scan Traffic Analysis (Wireshark)

### 🎯 Objective
Analyze TCP SYN packets to identify port scanning and reconnaissance activity from a SOC Level 1 perspective.

---

### 🧰 Tools Used
- Wireshark
- Windows 11
- Command Prompt

---

### 🧱 Environment
- OS: Windows 11
- Network Interface: Wi-Fi
- Capture Type: Live traffic

---

### 🔧 Lab Setup
1. Open Wireshark
2. Select Wi-Fi interface
3. Start packet capture
4. Generate connection attempts using Command Prompt
5. Stop capture after traffic is generated

---

### 🔍 Wireshark Display Filter
```bash
tcp.flags.syn == 1 && tcp.flags.ack == 0
```

---

### 📌 Questions & Answers
1. Which TCP flag is mostly observed?
   - Answer: SYN

2. Is there any ACK flag in response?
   - Answer: No ACK flag observed

3. Which protocol is used?
   - Answer: TCP

---

### 👀 Observations
- Multiple TCP SYN packets detected
- Different destination ports targeted
- No complete TCP three-way handshake
- Repeated SYN packets indicate probing behavior

---

### 🧠 Analysis
The observed traffic pattern is consistent with **port scanning or reconnaissance activity**.  
This behavior is often used by attackers to discover open ports and services.

---

### 🛡 SOC Use Case
SOC analysts monitor SYN-only traffic to:
- Detect early-stage attacks
- Identify scanning attempts
- Trigger IDS/IPS alerts
- Correlate with threat intelligence

---

### 🚨 Threat Assessment
- Activity Type: Reconnaissance
- Severity: Low
- Risk Level: Monitoring required

---

### 📸 Evidence
- Screenshot captured showing multiple SYN packets
- <img width="1920" height="1200" alt="Screenshot 2026-01-19 032649" src="https://github.com/user-attachments/assets/b147a2d5-7781-4e30-9087-69edd7faf3c9" />


---

### 📁 Artifacts Saved
- lab7-port-scan-analysis.pcapng
- Screenshot (.png)

---

### ✅ Lab Status
Completed successfully

---

### 🧠 Key Learning
- TCP SYN packets initiate connections
- SYN-only traffic can indicate scanning
- Wireshark filters help identify abnormal patterns
- SOC analysts rely on traffic patterns, not tools alone

## 🧪 Lab 8 – DHCP Traffic Analysis (Wireshark)

### 🎯 Objective
Analyze DHCP network traffic to understand how IP addresses are assigned and how SOC analysts identify abnormal DHCP behavior.

---

### 🧰 Tools Used
- Wireshark
- Windows 11
- Active Network Connection

---

### 🧱 Environment
- OS: Windows 11
- Network Interface: Wi-Fi
- Capture Type: Live Traffic

---

### 🔧 Lab Setup
1. Open Wireshark
2. Select the active Wi-Fi interface
3. Start packet capture
4. Connect to the network / renew IP address
5. Stop capture after DHCP traffic appears

---

### 🔍 Wireshark Display Filter
```bash
dhcp
```

---

### 📌 Questions & Answers
1. What type of DHCP message is observed?
   - Answer: BOOT REQUEST

2. What is the default gateway IP address?
   - Answer: 192.168.1.1

3. What is the destination IP address?
   - Answer: 255.255.255.255

4. Is the traffic suspicious?
   - Answer: No

---

### 👀 Observations
- DHCP Discover and Request packets observed
- Broadcast traffic used during IP assignment
- DHCP server responds correctly
- Normal IP leasing process detected

---

### 🧠 Analysis
The traffic represents a **normal DHCP process** where a client requests an IP address from a DHCP server.  
No abnormal behavior or rogue DHCP indicators were observed.

---

### 🛡 SOC Use Case
SOC analysts monitor DHCP traffic to:
- Detect rogue DHCP servers
- Identify unauthorized devices
- Monitor unusual IP assignments
- Investigate network misconfigurations

---

### 🚨 Threat Assessment
- Activity Type: Normal Network Operation
- Severity: None
- Risk Level: Safe

---

### 📸 Evidence
- Screenshot captured showing DHCP packets
- <img width="1920" height="1200" alt="Screenshot 2026-01-19 033120" src="https://github.com/user-attachments/assets/1c8cb9f2-6fbe-41f0-a360-ba64116b86e7" />


---

### 📁 Artifacts Saved
- lab8-dhcp-traffic-analysis.pcapng
- Screenshot 

---

### ✅ Lab Status
Completed successfully

---

### 🧠 Key Learning
- DHCP uses broadcast communication
- BOOT REQUEST initiates IP leasing
- DHCP analysis is critical in SOC investigations
- Normal traffic patterns help identify anomalies
- 
---

## 🔐 Section 6: Cryptography

This section focuses on cryptography fundamentals and password security concepts commonly encountered in defensive security and SOC environments.

### 🔹 Completed Rooms

- **Cryptography Basics**  
  Learned core cryptography concepts including encryption, confidentiality, and integrity.  
  👉 [View Notes](Cryptography/Cryptography-Basics.md)

- **Public Key Cryptography Basics**  
  Studied asymmetric encryption, public/private key pairs, and secure communication methods.  
  👉 [View Notes](Cryptography/Public-Key-Cryptography-Basics.md)

- **Hashing Basics**  
  Learned how hashing works, common algorithms, and why hashing is critical for password security.  
  👉 [View Notes](Cryptography/Hashing-Basics.md)

- **John the Ripper: The Basics**  
  Gained hands-on understanding of password cracking techniques and the importance of strong passwords.  
  👉 [View Notes](Cryptography/John-the-Ripper-The-Basics.md)

## Section 8: Web Hacking

In this section, I learned the fundamentals of web applications and how common web technologies work from a security perspective.

### Completed Rooms:
- Web Application Basics
- JavaScript Essentials
- SQL Fundamentals
- Burp Suite: The Basics

### Skills Gained:
- Understanding how web applications function
- Client-side scripting fundamentals
- Database basics and SQL concepts
- Intercepting and analyzing HTTP traffic
- Identifying common web security risks

This section strengthened my foundation in web technologies and web application security.

## Section 9: Offensive Security Tooling

This section focuses on commonly used offensive security tools and techniques to understand how attackers perform reconnaissance and exploitation.

### Completed Rooms:
- Hydra
- Gobuster: The Basics
- Shells Overview
- SQLMap: The Basics

### Skills Gained:
- Brute-force and password attack concepts
- Web and directory enumeration
- Understanding shells and post-exploitation access
- Automated SQL injection testing
- Recognizing offensive tooling from a defensive perspective

These labs improved my understanding of attacker techniques, helping me better analyze and defend against real-world threats.
---

## 🎯 Goal
To continue progressing towards **SOC Level 1** with a focus on defensive security and monitoring.


