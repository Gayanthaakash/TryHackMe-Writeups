# TryHackMe: Network Security Basics Walkthrough

## 🎯 Lab Objective
The objective of this module was to master foundational networking architecture, data encapsulation models, and communication protocols. For a security professional, network literacy is the bedrock of infrastructure defense; you cannot protect an environment or analyze traffic anomalies without completely understanding how data moves across wire topologies.

---

## 🔍 Core Networking Concepts Covered

### 1. Architectural Reference Models (OSI vs. TCP/IP)
Network communication relies on structured layering abstractions to process data traffic smoothly:
* **The OSI Model:** A conceptual 7-layer framework mapping data from physical electrical signals (Layer 1) up to consumer application interfaces (Layer 7).
* **The TCP/IP Model:** A streamlined 4-layer production standard (Network Interface, Internet, Transport, Application) that powers modern internet routing mechanics.

### 2. Encapsulation & Protocol Headers
As data travels down the stack, each layer wraps it with control definitions:
* **Transport Layer (TCP/UDP):** Segments data and adds source/destination port designations.
* **Network Layer (IP):** Packages segments into packets, embedding source and target IP logical addresses to manage cross-network routing pathways.
* **Data Link Layer (Ethernet):** Frames packets with physical MAC addresses to manage local hardware delivery across immediate switch switches.

### 3. Core Diagnostic Tooling & Protocols
* **ICMP (Internet Control Message Protocol):** Used for error reporting and network diagnostics.
* **Ping:** Utilizes ICMP Echo Requests to verify host availability and network latency properties.
* **Traceroute:** Maps the exact routing hop trajectory to a target machine by incrementally adjusting packet Time-to-Live (TTL) values.

---

## 🛠️ Enterprise Defensive Hardening & Infrastructure Controls
To build a resilient enterprise perimeter network using these architectural design principles, network security teams must enforce these controls:

1. **Implement Granular Network Segmentation:** Divide corporate networks into isolated Virtual Local Area Networks (VLANs) managed by strict Access Control Lists (ACLs). Demilitarized Zones (DMZs) must keep public-facing web instances safely separate from sensitive internal active directories.
2. **Deploy Network Intrusion Detection/Prevention Systems (IDS/IPS):** Enforce signature and anomaly-based traffic scanning tools (such as Snort or Suricata) at boundary choke points to inspect raw packet headers and payloads for known malicious exploit patterns.
3. **Enforce Network Access Control (NAC):** Utilize robust 802.1X authentication barriers to evaluate devices attempting to bridge onto corporate infrastructure, automatically isolating non-compliant or rogue rogue hardware instances.

---

## 📸 Visual Verification
*Below is my verified completion badge confirming the successful ingestion and execution of the Network Security Basics architecture framework:*<img width="1918" height="904" alt="Screenshot 2026-06-06 140941" src="https://github.com/user-attachments/assets/81ae6854-b963-4aee-a2b7-c085274830aa" />
