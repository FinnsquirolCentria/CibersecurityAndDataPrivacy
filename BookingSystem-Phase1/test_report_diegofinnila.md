# 1️⃣ Introduction

**Tester(s):**  
- Name: Diego Finnilä  

**Purpose:**  
The purpose of this penetration test is to identify security vulnerabilities and weaknesses in the Booking System (Phase 1) registration and login components. The goal is to assess the confidentiality, integrity, and availability risks related to user registration, authentication, and backend processing.

**Scope:**  
- **Tested components:**  
  - Registration page (`/register`)  
  - Login page (`/login`)  
  - API calls made during registration  
  - Client-side and server-side validation  
- **Exclusions:**  
  - Booking management functions  
  - Admin interfaces  
  - Payment system  
- **Test approach:**  
  - **Gray-box testing** (partial knowledge of the system, no source code)

**Test environment & dates:**  
- **Start:** 04.02.2026  
- **End:** 05.02.2026
- **Environment:**  
  - OS: Windows 11  
  - Browser: Chrome 121  
  - Docker Desktop

**Assumptions & constraints:**  
- No rate limiting or WAF in place  
- Database contains test/demo data only  
- Application intentionally vulnerable as part of coursework  
- Time allowed: ~2 hours  

---

# 2️⃣ Executive Summary

**Short summary:**  
Automated scanning (OWASP ZAP) and manual checks indicate multiple security and stability issues. The application returned frequent server errors (5xx) during testing. Because the registration endpoint often produced errors during attempts, some vulnerabilities (SQLi, XSS, plaintext password storage) could not be fully confirmed and require re-testing after stability fixes.

**Overall risk level:** High

**Top 5 immediate actions:**  
1. Fix application stability/server errors.
2. Add parameterized queries / prepared statements for all DB access.  
3. Add server-side input validation and sanitization.
4. Add CSRF protection and security headers (CSP, X-Frame-Options, X-Content-Type-Options, HSTS).  
5. After stability fixes, re-run automated scans and manual verification (focus: SQLi, XSS, password storage).

---

# 3️⃣ Severity scale & definitions

|  **Severity Level**  | **Description**                                                                                                              | **Recommended Action**           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
|      🔴 **High**     | A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution). | *Immediate fix required*         |
|     🟠 **Medium**    | A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF).                              | *Fix ASAP*                       |
|      🟡 **Low**      | A minor issue or configuration weakness (e.g., server version disclosure).                                                   | *Fix soon*                       |
| 🔵 **Info** | No direct risk, but useful for system hardening (e.g., missing security headers).                                            | *Monitor and fix in maintenance* |


---

# 4️⃣ Findings

| ID | Severity | Finding | Description | Evidence / Proof |
|----|----------|---------|-------------|------------------|
| F-01 | 🔴 High (Potential) | Possible SQL Injection (registration) | Automated tests and payloads indicated injection patterns but registration requests repeatedly returned server errors. Fll confirmation was not possible. Treat as high-priority until proven safe. | ![alt text](image.png) |
| F-02 | 🔴 High (Not Confirmed) | Password storage / exposure | Initial expectations suggested weak password handling, but registration often failed and responses were inconsistent. Manual interception was not reliably possible due to Error during registration. | Unable to reliably capture successful registration responses due to server errors. Recommendation: ensure passwords are never returned in API responses. |
| F-03 | 🟠 Medium (Potential) | Stored XSS via username | ZAP flagged absence of CSP and other protections; manual XSS confirmation could not be completed consistently because registration and rendering produced errors. Consider XSS possible where user-controlled content is rendered. | ZAP output (missing CSP) combined with observed response content suggests XSS risk. Recommendation: sanitize/encode output and add CSP. |
| F-04 | 🟠 Medium | Absence of Anti-CSRF tokens | ZAP reported "Absence of Anti-CSRF Tokens" for form endpoints. Forms or JSON endpoints used for registration do not include or validate CSRF tokens. | ZAP Alert: Absence of Anti-CSRF Tokens|
| F-05 | 🟠 Medium | Missing critical security headers | ZAP reported multiple missing headers: Content-Security-Policy (CSP) header not set, Missing Anti-clickjacking header, X-Content-Type-Options missing. | ZAP Alerts list and response header inspection.|
| F-06 | 🟡 Low | Application error disclosure / stability issues | The service returned multiple 5xx responses and an "Application Error Disclosure" alert in ZAP. Error responses contained details useful to an attacker (stack or DB error hints). | ZAP Alerts: Application Error Disclosure; Insights show a high percentage of 5xx responses for `http://localhost:8001`. |


---

# 5️⃣ Test limitations & next steps

- Registration endpoint returned frequent 5xx errors during testing; this prevented consistent manual verification of some vulnerabilities (SQLi, XSS, plaintext password exposure).  
- The ZAP automated scan produced a number of medium/low alerts (missing headers, CSRF absence, application error disclosure) which are reliable and should be fixed immediately.  
- Recommended immediate workflow:  
  - Fix application error.  
  - Implement basic hardening.  
  - Re-run OWASP ZAP full scan and manual verification of registration flow (intercept traffic with DevTools / Burp / ZAP proxy).  
  - If registration succeeds after fixes, run dedicated SQLi and XSS manual tests and confirm password handling/storage.

---

# 6️⃣ OWASP ZAP Test Report (Attachment)

**File:** [zap_report_round1.md](zap_report_round1.md)

---
