# Comprehensive Penetration Testing Report & Capstone

## Objective
Perform vulnerability assessment and penetration testing against a deliberately vulnerable environment.

## Environment

- DVWA
- Kali Linux Tools
- Nmap
- Wireshark
- Brave Browser

## Findings

### 1. Command Injection
Severity: Critical

The application fails to sanitize user supplied input before passing it to system commands.

Impact:
- Remote Code Execution
- Information Disclosure

Remediation:
- Input Validation
- Allowlisting
- Parameterized Command Execution

---

### 2. Brute Force Vulnerability
Severity: High

Default credentials were accepted and no account lockout controls were present.

Impact:
- Unauthorized Access

Remediation:
- MFA
- Account Lockout
- Password Policy

---

### 3. Security Misconfiguration
Severity: Medium

Application running at DVWA Low Security level.

Impact:
- Increased attack surface

Remediation:
- Harden configuration
- Disable insecure defaults

---

### 4. Open Ports
Severity: Medium

Nmap identified several exposed services.

Impact:
- Service enumeration
- Potential exploitation

Remediation:
- Close unnecessary ports
- Firewall filtering

---

### 5. Traffic Analysis
Severity: Informational

Network traffic captured and analyzed using Wireshark.

Purpose:
- Verify communications
- Identify protocols
