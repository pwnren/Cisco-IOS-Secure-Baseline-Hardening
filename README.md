# 🔐 Cisco IOS Secure Baseline Hardening

![Cisco IOS](https://img.shields.io/badge/Platform-Cisco%20IOS-blue)
![Security Baseline](https://img.shields.io/badge/Security-Baseline-critical)
![CIS Benchmark](https://img.shields.io/badge/Compliance-CIS%20Benchmark-success)
![Defense in Depth](https://img.shields.io/badge/Architecture-Defense--in--Depth-informational)
![Layer 2 Protection](https://img.shields.io/badge/Layer%202-Hardened-orange)
![VRF Segmentation](https://img.shields.io/badge/Segmentation-VRF%20Enabled-purple)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---
This repository provides a reusable security baseline for Cisco IOS network devices aligned with some STIG guidance and enterprise network security best practices.

The baseline reduces management-plane exposure, enforces centralized authentication, and implements Layer 2 protection controls.

# Security Domains Covered

## 🔐 Management Plane Security

- Disable insecure services (HTTP server, PAD, small TCP/UDP services)
- CDP control and exposure reduction
- SSHv2 only (4096 bit RSA key generation)
- Encrypted management transport exclusively
- TACACS+ centralized AAA (authentication, authorization, accounting)
- Local fallback authentication
- AES key encryption for sensitive credentials
- Exec timeout and session hardening
- Configuration archive logging

---

## 📊 Logging & Auditing

- Centralized syslog forwarding
- Buffered logging for local retention
- Timestamp enforcement (msec + timezone)
- SNMPv3 only (AuthPriv, no v1/v2c)
- Configuration change tracking
- Audit visibility for security monitoring platforms

---

## 🌐 Layer 2 Protection Controls

- Rapid PVST enabled
- PortFast default (access ports)
- BPDU Guard default
- Root Guard (rogue root prevention)
- Loop Guard (non designated port protection)
- UDLD aggressive (fiber protection)
- EtherChannel hardening (LACP active mode only)
- Port security (MAC limiting, sticky MAC, violation control)

---

## 🧱 Segmentation & Boundary Enforcement

- VRF based separation
- Layer 3 boundary control strategy
- ACL enforcement at trust boundaries
- No direct IT to OT routing without explicit policy
- Segmentation aware architecture design

---

# Design Principles

- Default deny security mindset
- Encrypted management plane only
- Least privilege access control
- Segmentation first architecture
- Defense in depth layering
- Compliance aligned implementation (CIS)
