# Cisco-IOS-Secure-Baseline-Hardening
Overview

This repository provides a reusable security baseline for Cisco IOS network devices aligned with STIG guidance and enterprise network security best practices.

The baseline reduces management-plane exposure, enforces centralized authentication, and implements Layer 2 protection controls.

## Management Plane Security
- Disable insecure services (HTTP, CDP, PAD)
- SSHv2 only (4096-bit RSA)
- TACACS+ AAA enforcement
- AES key encryption
- Exec-timeout configuration
- Legal login banner

## Logging & Auditing
- Centralized syslog forwarding
- Configuration archive logging
- Timestamp enforcement
- SNMPv3 only (no v2c)

## Layer 2 Protection
- Rapid-PVST enabled
- BPDU Guard default
- Root Guard
- Loop Guard
- UDLD aggressive
- EtherChannel (LACP only)

## Segmentation
- VRF separation 
- ACL boundary enforcement
- No direct IT-to-OT routing without policy

## Design Principles
- Default deny mindset
- Encrypted management access only
- Segmentation aware design
- Defense-in-depth layering
- Compliance alignment
