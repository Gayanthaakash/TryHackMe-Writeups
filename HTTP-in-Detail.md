# TryHackMe: HTTP in Detail Walkthrough

## 🎯 Lab Objective
The objective of this module was to analyze the core architecture of the HyperText Transfer Protocol (HTTP). Understanding request/response layers, header values, methods, and cookie state management is a critical prerequisite for identifying web application vulnerabilities and parsing web server security logs.

---

## 🔍 Core Security Concepts Analyzed

### 1. HTTP Request Methods & Risk Profiles
Web assets utilize different verbs to dictate actions. From a security perspective, understanding their behavior is critical:
* **GET:** Retrieves data. Parameters are sent directly inside the URL string, meaning sensitive data (like passwords or tokens) can be exposed in browser histories, reverse proxy logs, and referrer headers.
* **POST:** Submits data within the request body. This is the industry baseline for authentication or sensitive data transfers as it prevents parameter exposure in system logs.

### 2. HTTP Status Codes as Attack Indicators
Monitoring HTTP status codes allows security analysts to detect active reconnaissance or exploitation attempts:
* **2xx (Success):** Indicates normal operations or a successful exploit payload execution.
* **3xx (Redirection):** Can be manipulated by attackers for Open Redirect vulnerabilities if user input is unvalidated.
* **4xx (Client Errors):** A sudden spike in `404 Not Found` or `403 Forbidden` codes usually indicates an active directory brute-forcing scan (e.g., using tools like Gobuster).
* **5xx (Server Errors):** Code `500 Internal Server Error` often points to an unhandled application exception, which can be analyzed to discover SQL Injection or file inclusion flaws.

### 3. Session Management & Cookies
Because HTTP is a stateless protocol, cookies are injected into headers to track active sessions. Attackers target these via Cross-Site Scripting (XSS) to hijack user sessions.

---

## 🛠️ Defensive Remediation & Hardening Controls
To protect modern web infrastructure against structural protocol weaknesses, systems administrators should implement the following engineering controls:

1. **Enforce Global Transport Layer Security (TLS):** Upgrade all plain `HTTP (Port 80)` traffic to encrypted `HTTPS (Port 443)`. This encrypts the entire request/response architecture, preventing cleartext sniffing via Man-in-the-Middle (MitM) attacks.
2. **Implement Secure Cookie Flags:** Protect session tokens against interception or script theft by enforcing these attributes on the server:
   * `Secure`: Dictates that the cookie is *only* transmitted over encrypted HTTPS connections.
   * `HttpOnly`: Block access to the cookie via client-side JavaScript, nullifying standard Session Hijacking via XSS attacks.
   * `SameSite=Strict`: Limits cookie transmission to first-party contexts, mitigating Cross-Site Request Forgery (CSRF).
3. **Disable Information Disclosure:** Configure production web servers (Apache, Nginx, IIS) to suppress default banner headers (e.g., hiding exact software version names like `Server: Apache/2.4.41`) so threat actors cannot easily map known CVE exploits against the infrastructure.

---

<img width="1860" height="770" alt="Screenshot 2026-06-06 134255" src="https://github.com/user-attachments/assets/a9781f48-8126-4cd9-a2c6-23e9fa79e926" />

*Below is my verified completion badge confirming the successful ingestion and execution of the HTTP Protocol module:*
