# 🚨 DoS Attack Detection & SMS Alerting System

## 📘 Overview

This project provides a **real-time DoS attack detection system** that monitors network traffic and sends **SMS alerts** whenever suspicious packet activity is detected.
The system is built using:

* **Scapy** → for live packet sniffing
* **Twilio API** → for sending SMS alerts
* **Python** → for detection logic and automation

This repository contains a **refined and improved version** of the original concept, implemented as a standalone project for learning, testing, and SOC-based skill development.

---

## ✨ Features

### 🔍 Real-Time Network Monitoring

Continuously inspects incoming packets and tracks packet behaviour from different IP addresses.

### ⚠️ DoS Attack Identification

Detects possible DoS attacks by checking:

* Packet frequency
* Time window
* Abnormal spikes from any source IP

### 📱 SMS Notifications (Twilio)

Automatically sends an SMS alert when:

* A source IP crosses the defined packet threshold
* Suspicious behaviour is detected

### 🛠️ Customizable Parameters

Easily modify:

* Detection threshold
* Time window
* Interface to monitor
* SMS content

### 🚀 Easy Setup

Simple dependency installation and configuration steps to get started quickly.

---

## 🧰 Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Your-Repo-Name.git
cd Your-Repo-Name
```

---

## 2️⃣ Install Dependencies

### For Ubuntu/Debian

```bash
sudo apt update
sudo apt install python3-pip python3-scapy python3-twilio -y
```

### For Fedora

```bash
sudo dnf install python3-pip python3-scapy python3-twilio -y
```

### Python Dependencies

```bash
pip3 install -r requirements.txt
```

---

## 3️⃣ Configure Twilio Credentials

Update the placeholders in the script:

```python
ACCOUNT_SID = "YOUR_SID"
AUTH_TOKEN = "YOUR_AUTH_TOKEN"
TWILIO_PHONE_NUMBER = "YOUR_TWILIO_NUMBER"
TO_PHONE_NUMBER = "RECIPIENT_NUMBER"
```

> **Tip:** Prefer using environment variables instead of hardcoding credentials.

---

## ▶️ Running the Tool

Start detection:

```bash
python3 ddos-attack-tool.py
```

Once active, the system continuously monitors traffic and triggers alerts automatically.

---

## 📩 Example SMS Alert

```
⚠️ DoS Detected!
Source IP: 192.168.1.10
Packets: 80 in 5 seconds
Time: 2024-12-02 10:30:45
```

---

## 🔐 Security Best Practices

* Use **environment variables** for Twilio keys
* Run the tool **only on networks you own or have permission to monitor**
* Apply least-privilege principles
* Avoid exposing the script to the public with your credentials inside

---

## 🛠️ Future Enhancements

These improvements can be added later:

* Web dashboard for live statistics
* Multi-interface packet monitoring
* Automatic IP blocking (with iptables/Wazuh/SOC workflows)
* Persistent logging for audit and analysis

---

## 📘 About This Repository

This repository contains an **independent implementation** of a DoS detection + SMS alerting concept.
It has been rebuilt, cleaned, and structured in a new format to make it more professional, presentable, and usable in real SOC learning environments.

Suitable for:

* Cybersecurity students
* SOC analysts (beginner level)
* Python network-security practice
* Portfolio projects

---
