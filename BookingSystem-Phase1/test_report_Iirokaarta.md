# 1️⃣ Introduction

**Tester(s):**  
- Name:  Iiro Kaarta

**Purpose:**  
- Evaluate the security of the registeration flow and backend error handling.

**Test environment & dates:**  
- Start:  10:06 2.2.2026
- End:  ---
- Test Tool: Zap
- Target: http://localhost:8001
- Application type: Web application

**Assumptions & constraints:**  
- Local development environment (local host)

---

# 2️⃣ Executive Summary

The aplication includes several critical vunerabilities that should be fixed.
**Overall risk level:** (Low / Medium / High / Critical)

**Top 5 immediate actions:**  
1.  Implement serverside input validation
2.  Fix SQL injection vunerabilities
3.  Implement security headers
4.  Fix static file pahts and prevent internal errors from leaking to regular users
5.  Add csrf protection to all post forms

---

# 3️⃣ Severity scale & definitions

|  **Severity Level**  | **Description**                                                                                                              | **Recommended Action**           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
|      🔴 **High**     | A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution). | *Immediate fix required*         |
|     🟠 **Medium**    | A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF).                              | *Fix ASAP*                       |
|      🟡 **Low**      | A minor issue or configuration weakness (e.g., server version disclosure).                                                   | *Fix soon*                       |
| 🔵 **Info** | No direct risk, but useful for system hardening (e.g., missing security headers).                                            | *Monitor and fix in maintenance* |


---

# 4️⃣ Findings (filled with examples → replace)

> Fill in one row per finding. Focus on clarity and the most important issues.

| ID | Severity | Finding | Description | Evidence / Proof |
|------|-----------|----------|--------------|------------------|
| F-01 | 🔴 High | The username parameter is vunerable SQL injection|
| F-02 | 🔴 High | The username parameter is improperly validated and may allow directory traversal attacks|
| F-03 | 🟠 Medium | The registration form lacks an anti csrf token allowing attcakers to force authenticated users to submit unintended requests |
| F-04 | 🟠 Medium | The application does not set key headers |
| F-05 | 🟡 Low | Backend errors return generic 500 internal server error potentiaaly leaking internal application behavior|

---

# 5️⃣ OWASP ZAP Test Report (Attachment)

**Purpose:**  
- Attach or link your OWASP ZAP scan results (Markdown format preferred).
- https://github.com/Markkutosijaan/BookingSystem-Phase1/blob/main/BookingSystem-Phase1/zap_report_round1.md

