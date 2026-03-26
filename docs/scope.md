# Scope of Assessment

## 1. Target Information

- **Target URL:** http://testphp.vulnweb.com/
- **Scan Profile:** Deep-Safe Profile
- **Tool Used:** WebSentinel
- **Scan Type:** Automated Web Application Security Scan
- **Authentication Used:** No
- **Scan Mode:** Passive + Safe Active Testing

---

## 2. Objective

The objective of this assessment was to identify common web application security misconfigurations, vulnerabilities, and information disclosure issues using the WebSentinel deep-safe scanning profile without causing service disruption.

---

## 3. In-Scope Components

**The following components were included in scope:**

- Publicly accessible web pages
- Static and dynamic endpoints
- Form-based inputs **(GET & POST)**
- Query parameters
- Authentication-related pages **(login, signup)**
- AJAX endpoints
- Rewritten URL paths
- Image/file handler endpoints

---

## 4. Out of Scope

**The following were not included in this assessment:**

- Denial of Service (DoS) testing
- Brute force attacks
- Credential stuffing
- Infrastructure-level attacks
- Source code review
- Database-level exploitation
- Server-side shell access testing

---

## 5. Scan Coverage Summary

- Total Endpoints Discovered: **34**
- Maximum Crawl Depth: **3**
- HTTP Methods Tested: **GET, POST**
- Dynamic Endpoints Tested: **Yes**
- Form Inputs Tested: **Yes**

---

## 6. Limitations

- Results are based on automated scanning only.
- Manual penetration testing was not performed.
- Some vulnerabilities may require authenticated access.
- False positives/negatives may exist.
- No destructive payloads were executed due to safe scan mode.

---

## 7. Authorization Note

This scan was performed in a controlled learning environment against a deliberately vulnerable test application for educational and research purposes.