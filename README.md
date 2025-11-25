<p align="center">
  <img src="https://img.shields.io/badge/Prime%20Technologies%20Sdn.%20Bhd.-Security%20Controls%20Demonstration-0A84FF?style=for-the-badge&logo=shieldcheck&logoColor=white" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/IoT%20Security%20%7C%20MFA%20%7C%20API%20Rate%20Limiting%20%7C%20Firmware%20Integrity-1ABC9C?style=flat-square" />
</p>

Prime Technologies Sdn. Bhd. – Security Controls Demonstration

This repository contains three security demonstrations developed for a cybersecurity project focusing on the risks and defenses of an IoT/Smart Device company. The purpose of these demos is to show practical implementations of security controls that mitigate real threats identified through threat modelling and detailed risk assessment.

Prime Technologies Sdn. Bhd. (fictional) develops cloud-connected IoT devices such as smart locks, sensors, and lighting systems. These demos illustrate how the organization can strengthen its cybersecurity posture using modern, industry-standard security practices.

📌 Project Overview

Through the STRIDE threat modelling framework and detailed risk analysis, the following high-risk issues were identified:

Weak authentication → Credential theft

API exposure → Denial-of-Service (DoS) attacks

Insecure firmware update mechanism → Firmware tampering

Lack of authenticity checks → Supply-chain attacks

This repository demonstrates three security controls designed to address these issues:

Multi-Factor Authentication (MFA)

API Rate Limiting (DoS Mitigation)

Firmware Integrity & Digital Signature Verification

🚀 Demonstrations Included
1. Multi-Factor Authentication (MFA) Demo

Folder: mfa_demo/

This demo simulates a secure login system using:

Password authentication

A 6-digit TOTP code (Microsoft Authenticator / Google Authenticator)

A QR code popup for easy registration

🔐 Purpose

To prevent unauthorized access even if a password is compromised.

🛠 Tools Used

Python

pyotp

qrcode + Pillow

Microsoft Authenticator

📂 Files

mfa_demo.py — QR-based MFA login simulation

2. API Rate Limiting Demo

Folder: api_rate_limit_demo/

A Flask-based REST API demonstrating:

Normal API operation

Automatic blocking after excessive requests

HTTP 429 “Too Many Requests” responses

Optional attack simulation script

⚡ Purpose

To protect cloud APIs from DoS attacks and brute-force traffic.

🛠 Tools Used

Python

Flask

Flask-Limiter

(Optional) Postman / attacker script

📂 Files

api_rate_limit_demo.py

attack_script.py (optional)

3. Firmware Integrity & Digital Signature Verification (GUI Version)

Folder: firmware_security_demo/

This advanced demo validates IoT firmware using:

SHA-256 hashing (integrity)

RSA-PSS digital signatures (authenticity)

A Tkinter GUI for a visual demonstration

🔧 Purpose

To prevent malicious or tampered firmware from being installed on IoT devices.

🛠 Tools Used

Python

cryptography library

Tkinter

hashlib

📂 Files

gen_keys.py — generate RSA keys

sign_firmware.py — sign original firmware

firmware_gui_verify.py — GUI verification tool

firmware_original.bin

firmware_modified.bin

firmware_original.bin.sig

📁 Repository Structure
Project Source Codes/
│
├── api_rate_limit_demo/
│   ├── api_rate_limit_demo.py
│   └── attack_script.py
│
├── firmware_security_demo/
│   ├── gen_keys.py
│   ├── sign_firmware.py
│   ├── firmware_gui_verify.py
│   ├── firmware_original.bin
│   ├── firmware_modified.bin
│   └── firmware_original.bin.sig
│
├── keys/
│   ├── private_key.pem
│   └── public_key.pem
│
└── mfa_demo/
    └── mfa_demo.py

📦 Installation

Install all required dependencies:

pip install flask flask-limiter pyotp qrcode[pil] cryptography pillow

▶️ Running the Demos
MFA Demo
python mfa_demo/mfa_demo.py

API Rate Limiting Demo
python api_rate_limit_demo/api_rate_limit_demo.py

Firmware Integrity & Signature Demo
python firmware_security_demo/gen_keys.py
python firmware_security_demo/sign_firmware.py -i firmware_original.bin
python firmware_security_demo/firmware_gui_verify.py

🔒 Security Context

These demonstrations provide a layered security approach:

MFA → Secures user authentication

Rate Limiting → Protects cloud availability

Firmware Verification → Ensures device integrity & authenticity
