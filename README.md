# Cybersecurity-intern-task3

# 📊 Vulnerability Scan Report

This repository contains the vulnerability scan report generated on **September 25, 2025** using [HostedScan Security](https://hostedscan.com).  
The scan covered selected servers, networks, websites, and applications to identify potential security risks.

---

## 📌 Report Overview

- **Date of Scan:** September 25, 2025  
- **Tool Used:** HostedScan Security  
- **Total Targets Scanned:** 4  
- **Total Vulnerabilities Found:** 48 (0 Critical, 0 High, 28 Medium, 20 Low)  
- **Accepted Vulnerabilities:** 0  

---

## 🛡️ Key Findings

### 🔑 Executive Summary
- **Critical Vulnerabilities:** 0  
- **High Vulnerabilities:** 0  
- **Medium Vulnerabilities:** 28  
- **Low Vulnerabilities:** 20  
- Majority of issues are related to **web security headers, outdated libraries, and cookie configurations**.

---

### 🎯 Targets Scanned
| Target | Critical | High | Medium | Low | Accepted |
|--------|----------|------|--------|-----|----------|
| krct.ac.in | 0 | 0 | 22 | 10 | 0 |
| howtogeek.com (test URL) | 0 | 0 | 6 | 10 | 0 |
| 152.57.199.249 | 0 | 0 | 0 | 0 | 0 |
| krct.ac.in/ktgamin/assets/php/gallary/ | 0 | 0 | 0 | 0 | 0 |

---

### 🌐 Common Vulnerability Categories
- **Missing Security Headers**  
  - Absence of Anti-CSRF tokens  
  - Missing Anti-clickjacking header  
  - Strict-Transport-Security not set  
  - X-Content-Type-Options missing  

- **Weak Content Security Policy (CSP)**  
  - Wildcard directives  
  - `unsafe-inline` script and style usage  
  - CSP header not set  

- **Cookie & Session Issues**  
  - No `HttpOnly` flag  
  - No `SameSite` attribute  
  - No `Secure` flag  

- **Software & Library Issues**  
  - Vulnerable JS library: **Bootstrap 4.0.0**  

- **Information Disclosure**  
  - Private IP addresses exposed  
  - Server leaking version info via HTTP headers  

- **Open Ports**  
  - Medium-risk open ports: 21, 22, 25, 26, 53, 110, 143, 465, 587, 993, 995, 3306  
  - Low-risk open ports: 80, 443  

---

## 🚀 Recommendations

1. **Apply Security Headers**  
   - Implement `CSP`, `HSTS`, `X-Frame-Options`, and `X-Content-Type-Options`.  

2. **Harden Cookies**  
   - Add `HttpOnly`, `Secure`, and `SameSite` attributes to all session cookies.  

3. **Update Dependencies**  
   - Upgrade **Bootstrap** from v4.0.0 to the latest stable version.  

4. **Restrict Open Ports**  
   - Close unused ports (21, 25, 3306, etc.)  
   - Use firewalls and allow-listing to limit access.  

5. **Fix Information Disclosure**  
   - Remove private IPs and server version headers from responses.  

---

## 📂 Repository Structure
─ report.pdf   # Full vulnerability scan report (from HostedScan) ├── README.md    # Summary of findings and recommendations

---

## 📖 Glossary
- **CSRF** – Cross-Site Request Forgery  
- **CSP** – Content Security Policy  
- **HSTS** – HTTP Strict Transport Security  
- **OWASP** – Open Web Application Security Project  

---

## 📌 References
- [OWASP Security Headers](https://owasp.org/www-project-secure-headers/)  
- [CSP Documentation](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)  
- [Cookie Security Best Practices](https://owasp.org/www-community/controls/SecureCookieAttribute)  

---

## ✅ Conclusion
The scan found **no critical or high-risk issues**, but several **medium and low severity vulnerabilities** need to be addressed.  
Fixing these will **improve overall application security, protect against common attacks (XSS, CSRF, Clickjacking), and harden the server configuration**.
