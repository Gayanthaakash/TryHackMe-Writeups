# TryHackMe: Intro to Defensive Security Walkthrough

## 🎯 Lab Objective
The objective of this module was to explore the core operational responsibilities of defensive security structures (Blue Teaming). The practical exercises focused on threat identification, security monitoring architecture within a Security Operations Center (SOC), log analysis, and digital forensics fundamentals to protect enterprise infrastructure.

---

## 🔍 Core Defensive Concepts Covered

### 1. Security Operations Center (SOC) Functions
A SOC serves as a central hub monitoring organizational infrastructure for malicious patterns. Key activities analyzed include:
* **Log Ingestion:** Centralizing data from firewalls, endpoints, and servers to build operational visibility.
* **Alert Triaging:** Assessing real-time warning indicators to separate false positives from active system compromises.

### 2. Analytical Log Analysis
Log files provide the concrete historical trail of any digital interaction. During the lab, access logs were parsed to detect adversarial behavior:
* **Attack Footprints:** Identifying anomalous volume spikes, unusual HTTP methods, or unauthorized file requests which indicate directory enumeration or brute-force tracking attempts.

### 3. Threat Intelligence & Digital Forensics
* **Threat Intel:** Leveraging Indicators of Compromise (IoCs) such as known malicious IP addresses, domain names, and file hashes to block threats before execution.
* **Forensics:** Collecting architectural evidence post-incident while maintaining strict data integrity baselines to analyze the scope and root cause of a system breach.

---

## 🛠️ Enterprise Defensive Hardening Controls
To implement robust corporate cyber defense architectures based on these operational pillars, organizations should execute the following controls:

1. **Deploy a Centralized SIEM Solution:** Integrate a Security Information and Event Management (SIEM) tool (such as Splunk or Microsoft Sentinel) to aggregate, correlate, and analyze log files globally from across the entire network architecture.
2. **Enforce Rigid Logging Policies:** Configure comprehensive audit tracking across all domain controllers, critical application servers, and corporate firewalls. Ensure logs are stored securely in write-once-read-many (WORM) storage environments to prevent modification by intruders.
3. **Establish an Incident Response Plan (IRP):** Formulate clean, automated playbooks for common threat alerts (like phishing or unauthorized access attempts) to ensure the SOC team can isolate compromised endpoints immediately and minimize business disruption.

---

<img width="1789" height="792" alt="Screenshot 2026-06-06 140637" src="https://github.com/user-attachments/assets/69c3f686-b6b1-48d2-a184-3e4e347333da" />

*Below is my verified completion badge and environment capture demonstrating the successful execution of the defensive security module:*
