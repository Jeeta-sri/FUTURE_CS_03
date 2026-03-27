# 🔐 API Security Risk Analysis – DemoCommerce REST API v2.4

## 📌 Project Overview
This project presents a **comprehensive API Security Risk Analysis** conducted on the *DemoCommerce REST API v2.4* as part of a cybersecurity internship.

The assessment was performed using a combination of **Black-Box and Grey-Box testing methodologies** to identify critical vulnerabilities across authentication, authorization, data exposure, rate limiting, and input validation.

The analysis simulates a real-world security audit and demonstrates how API weaknesses can directly impact business operations, compliance, and user trust.

---

## 🧪 Assessment Details

| Field | Details |
|------|--------|
| **Target System** | DemoCommerce REST API v2.4 |
| **Base URL** | https://api.democommerce.io/v2 |
| **Assessment Type** | Black-Box + Grey-Box Testing |
| **Scope** | Auth, Authorization, Data Exposure, Rate Limiting, Input Validation |
| **Report Date** | March 22, 2026 |
| **Total Findings** | 12 |

---

## 🚨 Risk Summary

| Severity | Count |
|----------|------|
| 🔴 Critical | 2 |
| 🟠 High | 3 |
| 🟡 Medium | 4 |
| ⚪ Low / Info | 3 |

### 🔥 Most Critical Issues
- Unauthenticated PII exposure via `/users` endpoint  
- JWT authentication bypass using `alg: none`  

---

## 🔍 Key Security Findings

### 🔴 Critical
- **Unauthenticated PII Exposure**  
  - Customer data (email, phone, address) accessible without login  
- **JWT Authentication Bypass**  
  - API accepts forged tokens (`alg: none`)

### 🟠 High
- Broken Object-Level Authorization (IDOR/BOLA)  
- No rate limiting on login (brute-force risk)  
- Sensitive data leakage in error messages  

### 🟡 Medium
- Excessive data exposure in responses  
- SQL Injection vulnerability in search endpoint  
- API keys exposed in URL parameters  
- Insecure object references  

### ⚪ Low
- Missing CORS policy  
- Verbose server headers  
- Lack of HTTPS enforcement  

---

## 📊 Business Impact

- Exposure of **Personally Identifiable Information (PII)**  
- Risk of **account takeover and fraud**  
- Violations of **DPDP Act 2023 & GDPR compliance**  
- Potential **financial and reputational damage**  
- Increased attack surface for malicious actors  

---

## 🛠️ Tools & Technologies Used

### 🔹 API Testing & Analysis
- Postman  
- Insomnia  
- cURL  

### 🔹 Security Testing
- OWASP ZAP  
- Burp Suite  
- sqlmap  
- Hydra (Brute-force testing)  

### 🔹 Analysis Tools
- Browser DevTools (Network Analysis)  
- jwt_tool (Token testing)  

### 🔹 Documentation
- Microsoft Word  
- PDF Reports  

---

## 🧠 Methodology

The assessment followed a structured approach:

1. **API Enumeration** – Identified endpoints  
2. **Authentication Testing** – Token validation & bypass attempts  
3. **Authorization Testing** – Checked access control (IDOR/BOLA)  
4. **Data Exposure Analysis** – Inspected sensitive data leakage  
5. **Input Validation Testing** – Tested SQL injection vectors  
6. **Rate Limiting Testing** – Simulated brute-force attacks  
7. **Error Handling Review** – Analyzed information leakage  
8. **Key Management Testing** – Evaluated API key handling  

---

## 🛡️ Remediation Highlights

- Enforce **JWT authentication with strict algorithm validation**  
- Implement **role-based access control (RBAC)**  
- Apply **rate limiting & CAPTCHA on login endpoints**  
- Use **parameterized queries to prevent SQL injection**  
- Remove sensitive data from API responses  
- Secure API keys using **Authorization headers**  
- Implement proper **error handling and logging**  

---

## 📄 Deliverable

A **professional API Security Risk Analysis Report** including:

- Detailed vulnerability breakdown  
- Risk classification (Critical / High / Medium / Low)  
- Proof of Concept (PoC)  
- Business impact explanation  
- Step-by-step remediation plan  


---

## 🚀 Key Skills Demonstrated

- API Security Testing  
- Vulnerability Assessment & Penetration Testing  
- Authentication & Authorization Analysis  
- Risk Classification & Business Impact Mapping  
- Security Documentation & Reporting  
- SaaS Security Fundamentals  

---

## 📈 Conclusion

The assessment revealed multiple **critical and high-risk vulnerabilities** that could allow unauthorized data access, privilege escalation, and large-scale attacks.

This project highlights the importance of **proactive API security testing** and demonstrates how proper controls can significantly reduce risk exposure.

---

## 👩‍💻 Author

**Srijeeta Dutta**  
Cyber Security Intern  

---
