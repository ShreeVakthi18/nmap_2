# Network Vulnerability & Attack Surface Audit

## Project Objective
This project demonstrates a **professional-grade network security audit**.  
Using Nmap, I mapped the attack surface of a Linux-based target host to identify exploitable services, outdated software versions, and potential security risks.

---

## Technical Evidence
- **Terminal Proof:** Nmap scan screenshots  
- **Raw Audit Log:** Detailed scan results for verification  
- **Critical Findings Analysis:** Structured table of risks

| Port | Service      | Finding                                     | Risk Level |
|------|-------------|--------------------------------------------|------------|
| 23   | Telnet      | Cleartext protocol detected. Vulnerable to sniffing/MITM. | CRITICAL |
| 80   | Apache 2.4.7| Outdated version. Known CVEs (Path Traversal, etc.)    | HIGH     |
| 445  | SMB         | Filtered port. Potential entry point for lateral movement | MEDIUM   |

---

## Methodology (Cisco Defense Framework)
- **Service Versioning:** Identify outdated services (Apache 2.4.7)  
- **OS Fingerprinting:** Determined target OS (Linux) to refine analysis  
- **Audit Logging:** Generated multi-format reports compatible with SOC workflows

---

## Remediation Recommendations
- **Disable Telnet:** Replace with SSH (Port 22) for encrypted remote access  
- **Patch Apache:** Upgrade to the latest stable version to mitigate known vulnerabilities  
- **Firewall Hardening:** Ensure Port 445 (SMB) is blocked from external traffic

---

## Key Learnings
- Understanding **attack surfaces** helps prioritize remediation  
- Structured logging is critical for **evidence collection and reporting**  
- Risk-based analysis improves security decision-making

---

## Author
Computer Science undergraduate focused on cybersecurity fundamentals, network defense, and Linux security.
