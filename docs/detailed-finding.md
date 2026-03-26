# Detailed Findings

This section provides technical details for each identified vulnerability category.

---

# 1. Reflected Cross-Site Scripting (XSS)

#### Vulnerability Title
Reflected XSS via form field `text`

#### Affected Endpoint
http://testphp.vulnweb.com/guestbook.php

#### Method
POST

#### Parameter
text

#### Severity
High

#### CWE
CWE-79

#### CVSS v3.1
7.4

#### Confidence
Probable

## Description
User-controlled input submitted through the `text` form field is reflected in the HTTP response without proper sanitization or output encoding. This allows execution of arbitrary JavaScript in the victim’s browser.

## Evidence
**Payload used:**

`<script>alert(1)</script>`

The payload was reflected in the response.

## Impact
- Session hijacking
- Credential theft
- Phishing attacks
- Defacement
- Redirection to malicious websites

---

# 2. Missing Strict-Transport-Security Header

## Severity
Medium

## CWE
CWE-693

## CVSS v3.1
5.3

## Confidence
Confirmed

## Description
Multiple endpoints are missing the `Strict-Transport-Security` (HSTS) header.

## Affected Areas
- Homepage
- index.php
- categories.php
- artists.php
- disclaimer.php
- cart.php
- guestbook.php
- userinfo.php
- privacy.php
- Mod_Rewrite_Shop endpoints

## Impact
**Without HSTS:**
- Users may be vulnerable to downgrade attacks
- Man-in-the-Middle (MITM) attacks become easier
- HTTPS enforcement is not guaranteed

---

# 3. Clickjacking Vulnerability

## Severity
Medium

## CWE
CWE-1021

## CVSS v3.1
4.3

## Confidence
Probable

## Description
**Pages lack protection mechanisms such as:**
- X-Frame-Options
- Content-Security-Policy (frame-ancestors)

This allows the site to be embedded inside an iframe on a malicious domain.

## Impact
- UI redressing attacks
- Invisible button overlays
- Forced user interaction
- Credential harvesting

---

# 4. Server Version Information Disclosure

## Severity
Low

## CWE
CWE-200

## CVSS v3.1
3.1

## Confidence
Confirmed

## Description
HTTP response headers disclose server and framework version details.

## Evidence
Server: **nginx/1.19.0**  
X-Powered-By: **PHP/5.6.40**

## Impact
- Assists attackers in vulnerability research
- Enables targeted exploitation
- Reduces security through information leakage

---

# Risk Concentration Analysis

**The majority of findings are configuration-related, indicating:**

- Weak security hardening
- Default server configurations
- Missing defensive headers

However, the presence of a High severity XSS vulnerability significantly increases exploitation risk.