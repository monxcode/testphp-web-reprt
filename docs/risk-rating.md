# Risk Rating Model

This project uses a structured internal risk classification model based on severity, impact, and exploitability.

## Risk Calculation Factors

**Each vulnerability was evaluated based on:**

- Technical Impact
- Exploitability
- Affected Component
- Data Sensitivity
- Exposure Level
- Authentication Requirement

## Severity Levels

### Critical
- Remote code execution
- Authentication bypass
- Direct database compromise
- Full account takeover
- Sensitive data exfiltration without authentication

### High
- SQL Injection
- Stored XSS
- Broken Access Control
- File Inclusion vulnerabilities
- Privilege escalation

### Medium
- Reflected XSS
- Security misconfigurations
- Missing access restrictions
- Partial data exposure
- Insecure direct object references

### Low
- Missing security headers
- Server version disclosure
- Clickjacking vulnerability
- Minor information leakage

### Informational
- Technology stack disclosure
- Debug traces
- Non-exploitable misconfigurations

## Overall Risk Overview

- Total Vulnerabilities: **41**
- Security Score: **46%**
- Risk Posture: **High Exposure**

The application demonstrates significant attack surface presence and would be considered high-risk in a real-world production scenario.