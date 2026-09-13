# Network Footprinting & Network Scanning — Week 2

## Executive Summary
This repository contains the technical deliverables, raw evidence, and official Penetration Testing Report for Week 2 of the Networkwalks Cybersecurity & Ethical Hacking Program. The project covers passive external footprinting of `networkwalks.com` using native Kali Linux reconnaissance utilities and internal network discovery using Zenmap on a Windows host.

---

## Project Module 1: Footprinting & Reconnaissance (Kali Linux)
Passive reconnaissance was conducted against `networkwalks.com` across six primary targets:

1. **WHOIS Lookup (`whois`):** Extracted domain registration metadata, creation/expiration dates, and HostGator name servers (`ns6135.hostgator.com`, `ns6136.hostgator.com`).
2. **Web Technology Fingerprinting (`whatweb`):** Identified the underlying web stack including WordPress 7.0.4, WP Download Manager 3.3.58, Apache HTTP Server, Bootstrap 7.0.4, and jQuery 3.7.1.
3. **DNS Resolution (`nslookup`):** Resolved the target domain `networkwalks.com` to its public IPv4 address (`192.232.216.135`).
4. **HTTP Header Analysis (`curl -I`):** Inspected response headers to extract server banners (`Apache`), caching behavior (`x-nginx-cache: WordPress`), and exposed REST API routes (`/wp-json/`).
5. **WAF Detection (`wafw00f`):** Detected an active Web Application Firewall protecting the application: **ModSecurity (SpiderLabs)**.
6. **DNS Enumeration (`dnsrecon`):** Mapped public DNS zone records including NS records, MX mail servers (`mail.networkwalks.com`), SPF policies, and cPanel service (SRV) records.

---

## Project Module 5: Network Scanning with Zenmap (Windows Host)
Active network discovery was conducted across the local LAN on the Windows host machine:

1. **Subnet Profiling (`ipconfig`):** Identified the local host IPv4 address (`192.168.86.35`) and the `/24` network range (`192.168.86.0/24`).
2. **Host Discovery Scan (`nmap -sn`):** Executed a Ping Scan across `192.168.86.0/24` to discover active hosts without port scanning.
3. **Asset & MAC Enumeration:** Documented IP and hardware MAC addresses for all responding live hosts.
4. **Topology Generation:** Visualized and exported the network topology layout in PDF format (`topology.pdf`).

---

## Final Penetration Testing Report (W2-PM-FINAL)
The formal penetration testing report consolidates all findings from both PM1 and PM5 into an executive-ready security assessment:

* **Scope & Authorizations:** Documented written permissions and target boundaries for `networkwalks.com` and local LAN testing.
* **Risk Analysis Matrix:** Formatted findings into structured risk levels evaluating public information disclosure and infrastructure exposures.
* **Strategic Recommendations:** Actionable defense strategies covering HTTP header hardening, CMS patch management, WAF rule tuning, and periodic internal network audits.
* **Evidence Log:** Complete mapping of all screenshot proofs and terminal logs backing up each reported finding.

---

## Repository Contents
* **Penetration Testing Report:** The compiled report detailing all findings, risk assessments, and recommendations.
* **Network Topology:** Graphical network layout exported in PDF format from Zenmap.
* **Terminal Logs:** Text file containing raw output logs for all executed commands across Kali Linux and Windows.
* **Visual Evidence:** Screenshot verifications documenting command executions and scan results for each task.

---
**Student:** Muhammad Zain Ul Abiddin  
**Batch:** B083A  
**Program:** Networkwalks Cybersecurity & Ethical Hacking
