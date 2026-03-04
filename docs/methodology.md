# Methodology

## 1. Assessment Approach

This assessment was conducted using the **WebSentinel** automated security scanner with the **Deep-Safe** profile enabled.

The methodology followed a structured black-box testing approach, meaning no source code or internal architecture access was used during the scan.

---

## 2. Scanning Phases

### Phase 1 – Target Initialization
- Target URL validation
- DNS resolution
- Initial HTTP connectivity check
- Technology fingerprinting (Server & Framework detection)

---

### Phase 2 – Crawling & Endpoint Discovery
- Recursive link crawling
- Dynamic URL detection
- Query parameter mapping
- Form extraction (GET & POST)
- Authentication page identification
- AJAX endpoint detection
- URL rewrite path discovery

Maximum crawl depth reached: **3**

---

### Phase 3 – Passive Analysis
The following checks were performed without injecting aggressive payloads:

- HTTP security header analysis
- Server version disclosure detection
- Information leakage via response headers
- Clickjacking protection checks
- SSL enforcement validation

---

### Phase 4 – Safe Active Testing
Non-destructive payloads were used to detect:

- Reflected Cross-Site Scripting (XSS)
- Input reflection behavior
- Parameter handling anomalies
- Form submission validation weaknesses

No destructive or high-impact payloads were executed.

---

## 3. Vulnerability Classification

Identified issues were categorized based on:

- Severity (Low, Medium, High)
- CWE (Common Weakness Enumeration)
- CVSS v3.1 Score
- Exploitability (Passive / Probable)
- Confidence Level (Confirmed / Probable)

---

## 4. Risk Rating Model

Risk levels were determined using:

- CVSS score
- Impact potential
- Exploit complexity
- Exposure surface
- Confidence rating

---

## 5. Testing Constraints

- No authentication credentials were used.
- No brute force or DoS attempts performed.
- No manual exploitation beyond safe payload reflection testing.
- Scan conducted in safe-mode to avoid service disruption.

---

## 6. Tools & Environment

- Tool: WebSentinel
- Profile: Deep-Safe
- Mode: Automated Black-Box
- Output Formats: JSON, PDF

---

## 7. Assurance Level

This assessment provides automated vulnerability detection results.
Manual validation is recommended for production-level security assurance.