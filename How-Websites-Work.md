# TryHackMe: How Websites Work Walkthrough

## 🎯 Lab Objective
The objective of this module was to break down the technical components that dictate web application behavior. From a cybersecurity perspective, understanding how browsers request, resolve, and render web assets is an absolute prerequisite for testing web layer vulnerabilities (like Cross-Site Scripting or SQL Injection) and implementing defensive proxy architectures.

---

## 🔍 Core Web Architecture Concepts Covered

### 1. The Domain Name System (DNS) Translation
Computers communicate using IP logical routing addresses, but humans utilize domain strings. DNS acts as the phonebook of the web:
* **Mechanism:** A multi-tiered request structure (Root servers, TLD servers, and Authoritative Name Servers) resolves a human-readable domain name (e.g., `tryhackme.com`) into an accessible IP address.
* **Security Context:** Unsecured DNS requests are vulnerable to interception and spoofing attacks, highlighting the industry requirement for monitoring recursive resolver logs.

### 2. Anatomy of an HTTP Request Layer
Browsers generate automated network requests using structural header definitions:
* **Headers:** Pass metadata context such as the client environment configuration (`User-Agent`), supported content structures, and active authorization states or session cookies.
* **Risk Factor:** Attackers manipulate input parameters inside headers or query strings to trick backend web server databases into executing unauthorized logic queries.

### 3. Client-Side Rendering Tech (HTML / CSS / JavaScript)
Once the server approves an HTTP request, it delivers a payload to be rendered inside the client browser environment:
* **HTML:** Defines the document infrastructure skeleton.
* **CSS:** Dictates visual style presentation metrics.
* **JavaScript:** Executes client-side application logic. Because JavaScript runs directly inside the client's local context, attackers target it to run unauthorized scripts via Cross-Site Scripting (XSS).

---

## 🛠️ Enterprise Web Architecture Hardening Controls
To secure modern web infrastructure and prevent protocol exploitation, network security architecture teams must enforce these controls:

1. **Implement Global DNSSEC (Domain Name System Security Extensions):** Deploy cryptographic signatures across corporate authoritative DNS zones. This validates that the resolution data sent to client browsers is authenticated and hasn't been altered by a middleman attack.
2. **Deploy an Authoritative Content Security Policy (CSP):** Enforce strict `Content-Security-Policy` HTTP headers on the server side to tell browsers exactly which source domains are authorized to execute scripts on the webpage. This effectively mitigates data theft from XSS vulnerabilities.
3. **Audit Web Banners and Information Leakage:** Harden production web application layouts to obscure exact system infrastructure versioning tags from public header packets, preventing attackers from conducting automated exploit mapping scans against the domain.

---

<img width="1919" height="915" alt="Screenshot 2026-06-06 141039" src="https://github.com/user-attachments/assets/2e67d888-00a9-46aa-8a19-0dbb59ecf674" />

*Below is my verified completion badge confirming the successful ingestion and execution of the How Websites Work architectural framework challenge:*
