# Endpoints Analysis

## 1. Overview

During the Deep-Safe scan, WebSentinel discovered multiple static and dynamic endpoints across the application.

Total Endpoints Identified: **34**  
Maximum Crawl Depth: **3**  
HTTP Methods Observed: **GET, POST**  

---

## 2. Endpoint Classification

| Type       | Count | Description |
|------------|--------|------------|
| Static     | 8      | Standard content pages |
| Dynamic    | 20     | Parameterized & rewritten URLs |
| Auth       | 2      | Login & Signup related pages |
| AJAX       | 1      | Asynchronous content endpoint |
| File-based | 1      | File/image handler |

---

## 3. High-Risk Endpoints

#### guestbook.php
- Method: **POST**
- Forms: **1**
- Vulnerability: **Reflected XSS**
- Risk Level: **High**

#### product.php?pic=1
- Parameter: **pic**
- Dynamic content rendering
- Potential injection surface

#### showimage.php?file=
- Parameter: **file**
- File handling endpoint
- Potential path manipulation surface (no exploitation confirmed)

---

## 4. Parameterized Endpoints

**The following parameters were identified during crawling:**

- cat
- artist
- pp
- pic
- file
- size

**These parameters represent potential input vectors for:**
- Injection attacks
- File inclusion
- Parameter tampering
- Business logic abuse

---

## 5. Authentication Surface

**Identified authentication-related pages:**

- login.php
- signup.php
- secured/newuser.php

**Forms detected:**
- Login forms
- Account creation forms
- User information submission forms

No authentication bypass attempts were performed.

---

## 6. Dynamic Routing Areas

**Rewritten URL structures discovered:**

- /Mod_Rewrite_Shop/
- /Details/{product}/{id}/
- /BuyProduct-{id}/
- /RateProduct-{id}.html

These endpoints dynamically render product content and represent additional attack surface.

---

## 7. Exposure Analysis

**Key observations:**

- Multiple dynamic endpoints without security headers
- File-serving endpoints exposed publicly
- POST endpoints accepting user input
- No visible rate limiting mechanisms detected

---

## 8. Attack Surface Summary

**The application exposes:**

- Form-based inputs
- URL parameters
- File handlers
- Authentication interfaces
- Dynamic routing mechanisms

Combined with missing security headers, this significantly increases exposure risk.