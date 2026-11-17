
Penetration test report for DC-1 (VulnHub)
# DC-1 VAPT Report

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Target](https://img.shields.io/badge/Target-DC--1-blue)
![CVSS](https://img.shields.io/badge/Critical-CVE--2018--7600-red)

## Overview
Penetration test report for DC-1 (VulnHub lab environment).  
Full compromise chain: unauthenticated RCE → DB credentials leak → SUID privilege escalation → root.

## Findings Summary
| ID | Title | Severity | CVSS |
|----|-------|----------|------|
| PT-01 | Drupalgeddon2 RCE | Critical | 9.8 |
| PT-02 | Config file exposure | High | 7.5 |
| PT-03 | DB credential disclosure | High | 8.1 |
| PT-04 | SUID privilege escalation | Critical | 9.1 |
| PT-05 | Weak auth controls | Medium | 5.3 |
| PT-06 | Unrestricted file access | Medium | 5.5 |
| PT-07 | Unnecessary services | Low | 4.3 |

## Methodology
1. **Recon** — Nmap scan, Drupal 7 fingerprint
2. **Initial Access** — CVE-2018-7600 via Metasploit
3. **Privilege Escalation** — SUID binary abuse → root shell

## Tools
- Nmap, Metasploit Framework, MySQL client

## Disclaimer
This report is for educational purposes only. The target is a legal VulnHub lab environment. Do not use these techniques against systems without explicit permission.
