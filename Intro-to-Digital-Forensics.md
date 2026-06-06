# TryHackMe: Intro to Digital Forensics Walkthrough

## 🎯 Lab Objective
The objective of this module was to explore the fundamental processes behind digital forensics investigations. The exercises focused on identifying digital footprints left behind by threat actors, analyzing file artifacts, understanding metadata structures, and maintaining data integrity to build a legally defensible timeline of an incident.

---

## 🔍 Core Forensics Concepts Covered

### 1. The Forensic Process & Chain of Custody
Digital forensics requires a strict methodology to ensure evidence is admissible in a court of law or internal corporate review:
* **Acquisition:** Capturing raw data from volatile memory (RAM) or non-volatile storage without modifying the original source material.
* **Chain of Custody:** Documenting a chronological history of everyone who collected, handled, and analyzed the target hardware or image file to ensure no tampering occurred.

### 2. Artifact & Metadata Analysis
Files contain hidden tracking structures that reveal details about an attacker's actions:
* **Metadata:** Analyzing document properties to identify author names, embedded software versions, configuration details, and creation/modification timestamps.
* **Hex & Magic Bytes:** Inspecting raw hexadecimal values to verify true file types (e.g., detecting if an attacker renamed a malicious executable `.exe` file to a harmless text `.txt` extension to bypass security screening).

---

## 🛠️ Enterprise Defensive Hardening & Response Controls
To maintain high forensic readiness across enterprise infrastructure, organizations should implement the following security controls:

1. **Deploy Immutable Host Logging:** Secure host endpoint logs by shipping them off the asset in real-time to a central storage tier. Threat actors frequently attempt to clear local Windows Event Logs or Linux syslog files to erase their footprints post-compromise.
2. **Utilize Standardized Write-Blockers:** Ensure response teams connect target storage drives strictly via hardware or software write-blockers during evidence duplication. This prevents the host operating system from automatically overwriting metadata or hidden configuration parameters.
3. **Establish Cryptographic Baseline Hashing:** Generate immediate cryptographic hashes (e.g., SHA-256) of all acquired drive images and evidence files right at the collection stage. Recalculating these hashes throughout the analysis cycle ensures data integrity remains completely untampered.

---

## 📸 Visual Verification
*Below is my verified completion badge confirming the successful ingestion and execution of the Digital Forensics fundamentals path module:*<img width="1858" height="725" alt="Screenshot 2026-06-06 140813" src="https://github.com/user-attachments/assets/2c367c5e-0ab0-41ed-ae92-d36fd383c7cc" />
