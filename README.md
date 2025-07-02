# MAC Changer – Enhancing Network Security through MAC Address Spoofing

## 📌 Overview
This project demonstrates the use of the `macchanger` tool in Kali Linux to simulate MAC address spoofing, and the detection of such activities using Wazuh SIEM. The project was conducted as part of a cybersecurity internship (Skillogic, Phase 3) with a goal to enhance endpoint visibility and security monitoring.

## 🎯 Objectives
- Simulate MAC address spoofing in a virtual lab environment
- Detect spoofed MAC changes using Wazuh SIEM
- Understand how attackers can evade MAC-based restrictions
- Validate the importance of endpoint visibility in network security

## 🧰 Tools Used
- **macchanger**: To perform MAC address spoofing
- **Kali Linux 2023.4**: Host system for the spoofing activity
- **Wazuh SIEM**: To detect changes in MAC addresses and monitor logs
- **VirtualBox**: Lab environment for testing
- **ifconfig / ip**: For interface configuration

## 🔍 Methodology
1. **Lab Setup**: Configured VirtualBox with Kali Linux and Wazuh Manager OVA.
2. **Wazuh Agent Installation**: Installed and registered the agent on Kali VM.
3. **MAC Spoofing Simulation**:
   - Brought down the interface (eth0)
   - Spoofed MAC using `macchanger -r`
   - Reactivated interface
4. **Detection Phase**: Used Wazuh dashboard to monitor and confirm MAC spoofing activity.

## 📸 Proof of Concept
- Successful change from real MAC to spoofed MAC (`08:00:27:7d:37:07` → `00:11:22:33:44:55`)
- Detection confirmed on Wazuh with agent logs
- Screenshot logs attached in report

## 📊 Key Findings
- MAC address spoofing can bypass basic access controls
- Wazuh SIEM can detect hardware-level changes at the endpoint
- Endpoint agents enhance visibility in a SOC environment

## ✅ Outcome
This simulation validated the effectiveness of MAC spoofing and how it can be monitored using a SIEM. It reinforced the importance of real-time endpoint monitoring and anomaly detection for network security teams.

## 📄 Report
[Click here to view the full PDF report](./Project_Report_MAC_Changer.pdf)

## 👨‍💻 Contributors
- Siddharth Anilrao Lone
- Prasad Jadhav
- Mayureshwar Kulkarni
- Pravin Rathod
