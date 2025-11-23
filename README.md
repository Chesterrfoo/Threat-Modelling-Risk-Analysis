# Prime Technologies Sdn. Bhd. Security Controls Demonstration

This repository contains three security demonstrations developed for a cybersecurity project focusing on the risk analysis and protection of an IoT/Smart Device company. The goal of this repository is to showcase practical implementations of critical security controls that address real threats identified through threat modelling and detailed risk assessment.

These demos simulate how an IoT provider like SmartHomeX can strengthen its security posture against credential theft, API abuse, firmware tampering, and device-level threats.

---

## 📌 Project Overview

Prime Technologies Sdn. Bhd. is a fictional IoT/Smart Device company used for academic analysis.  
The company manages cloud-connected IoT devices such as smart locks, sensors, and lighting systems.

Through threat modelling (STRIDE) and detailed risk assessment, several high-risk vulnerabilities were identified:

- Weak authentication leading to credential theft  
- Cloud API exposure to DoS attacks  
- Insecure firmware update mechanism  
- Lack of device integrity validation  

This repository contains three code-based demonstrations showing how these risks can be mitigated effectively.

---

# 🚀 Demonstrations Included

## 1. Multi-Factor Authentication (MFA) Demo
**Folder:** `/mfa_demo/`

This demo simulates a login system that requires:

- Correct password  
- A valid 6-digit time-based one-time password (TOTP)

The system is compatible with:
- Google Authenticator  
- Authy  
- Microsoft Authenticator  

### 🔐 Purpose  
To prevent unauthorized access even if an attacker steals user credentials.

### 🛠 Tools Used  
- Python  
- `pyotp` for TOTP generation  
- `qrcode` for Google Authenticator QR setup  

### 📂 Files  
- `mfa_qr_demo.py` – MFA demo with QR code integration  
- `mfa_demo.py` – Basic MFA login simulation  

---

## 2. API Rate Limiting Demo
**Folder:** `/rate_limit_demo/`

A simple Flask-based REST API that demonstrates:

- Normal API access  
- Service failure under request flooding  
- Rate limiting protection using `Flask-Limiter`

### ⚡ Purpose  
To protect cloud APIs from Denial-of-Service (DoS) and brute-force attacks.

### 🛠 Tools Used  
- Python  
- Flask  
- Flask-Limiter  
- (Optional) Postman for request spamming  

### 📂 Files  
- `rate_limit_demo.py` – API endpoint with rate limiting enabled  

---

## 3. Firmware Integrity Verification Demo
**Folder:** `/firmware_hash_demo/`

This demo simulates the verification of IoT firmware before installation using SHA-256 hashing.

It compares:

- `firmware_original.bin`  
- `firmware_modified.bin`  

If the hashes differ → device rejects the firmware.

### 🔧 Purpose  
To prevent firmware tampering and supply-chain attacks.

### 🛠 Tools Used  
- Python  
- `hashlib` (built-in SHA-256 hashing)  
- Sample firmware files  

### 📂 Files  
- `firmware_hash_demo.py`  
- `firmware_original.bin`  
- `firmware_modified.bin`  

---

# 📦 Installation

Install the required dependencies:

```bash
pip install flask flask-limiter pyotp qrcode[pil]
