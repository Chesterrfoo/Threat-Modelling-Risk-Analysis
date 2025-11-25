# Prime Technologies Sdn. Bhd. – Security Controls Demonstration

This repository contains three security demonstrations developed for a cybersecurity project focusing on protecting an IoT/Smart Device ecosystem. 
The purpose of this repository is to showcase practical implementations of security controls that mitigate real threats discovered through threat modelling and detailed risk assessment.

Prime Technologies Sdn. Bhd. (fictional) builds cloud-connected IoT devices such as smart locks, sensors, and lighting systems. 
These demonstrations illustrate how the company can strengthen its cybersecurity posture using modern, industry-standard security measures.

---

## 📌 Project Overview

Through the STRIDE threat modelling framework and detailed risk analysis, the following high-risk issues were identified:

- **Weak authentication** → Credential theft  
- **API exposure** → Denial-of-Service (DoS) attacks  
- **Insecure firmware update mechanism** → Firmware tampering  
- **Lack of authenticity checks** → Supply-chain attacks  

This repository demonstrates three major security controls developed to address these risks:

- **Multi-Factor Authentication (MFA)**  
- **API Rate Limiting (DoS Mitigation)**  
- **Firmware Integrity & Digital Signature Verification**

---

# 🚀 Demonstrations Included

---

## 1. Multi-Factor Authentication (MFA) Demo  
**Folder:** `mfa_demo/`

A secure login simulation using:

- Password authentication  
- A 6-digit TOTP code (Microsoft / Google Authenticator)  
- A QR code popup for easy account registration  

### 🔐 Purpose
To prevent unauthorized access even if a password is compromised.

### 🛠 Tools Used
- Python  
- `pyotp`  
- `qrcode[pil]`  
- `Pillow`  
- Microsoft Authenticator  

### 📂 Files
- `mfa_demo.py` — Complete QR-based MFA simulation

---

## 2. API Rate Limiting Demo  
**Folder:** `api_rate_limit_demo/`

A Flask-based REST API demonstrating:

- Normal endpoint access  
- Automatic blocking after excessive requests  
- HTTP 429 “Too Many Requests” error  
- Optional attacker script to simulate DoS traffic  

### ⚡ Purpose
To protect cloud APIs from denial-of-service attempts and brute-force request floods.

### 🛠 Tools Used
- Python  
- Flask  
- Flask-Limiter  
- (Optional) Postman or Python attacker script  

### 📂 Files
- `api_rate_limit_demo.py`  
- `attack_script.py` (optional attacker simulation)

---

## 3. Firmware Integrity & Digital Signature Verification (GUI Version)  
**Folder:** `firmware_security_demo/`

An enhanced IoT firmware security demo featuring:

### ✔ SHA-256 hashing  
Detects any change in firmware (integrity).

### ✔ RSA-PSS digital signature verification  
Validates firmware authenticity.

### ✔ Tkinter GUI  
User-friendly graphical interface for demonstrating both integrity and signature verification.

### 🔧 Purpose
To prevent malicious or tampered firmware from being installed on IoT devices — a critical requirement in modern OTA (Over-The-Air) update systems.

### 🛠 Tools Used
- Python  
- `cryptography` (RSA key generation, signing, verification)  
- `hashlib`  
- Tkinter  

### 📂 Files
- `gen_keys.py` — Generates RSA private & public keys  
- `sign_firmware.py` — Signs original firmware to produce `.sig`  
- `firmware_gui_verify.py` — GUI tool for verifying firmware integrity & signature  
- `firmware_original.bin`  
- `firmware_modified.bin`  
- `firmware_original.bin.sig`  

---

# 📁 Repository Structure

