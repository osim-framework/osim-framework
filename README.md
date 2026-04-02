# OSIM — Orthogonal Systems Invariance Method

> "Detection without containment is forensics, not security."

A production-grade Zero Trust security architecture framework for 
designing, enforcing, and validating security boundaries under 
adversarial conditions.

**Author:** Alec Sanchez  
**Version:** 1.0 — 2026  
**Status:** Active Development

---

## What OSIM Is

OSIM defines how security zones are constructed, governed, and 
validated so that compromise of one zone cannot propagate to 
adjacent zones through implicit trust channels.

Built and validated against a production on-premises lab environment 
running OPNsense, Proxmox, Wazuh, TheHive, MISP, and a full 
Windows Server 2022 Active Directory domain.

---

## Core Properties

- Default-deny enforcement at every zone boundary
- Machine-verifiable security invariants
- ATT&CK-mapped threat model
- Red team validated controls
- Firewall as code governance
- 12-VLAN segmented architecture with explicit inter-zone policy

---

## Lab Architecture

| Node | Role | Key Tools |
|------|------|-----------|
| P520 (64GB) | Blue team / SOC | Wazuh, TheHive, MISP, Greenbone, Velociraptor |
| T480 (48GB) | Red team / Attack | Kali Purple, Sliver C2, REMnux, CAPE |
| T620 | Firewall | OPNsense 26.1.5, Suricata 8.0.4 |
| Cisco 3560CX | Switching | 12 VLANs, 802.1Q trunk |

---

## Detection Stack

- **SIEM:** Wazuh 4.x — agent-based EDR + log aggregation
- **Case Management:** TheHive 5.4 — incident response workflows  
- **Threat Intel:** MISP 2.4 — IOC enrichment and sharing
- **Vuln Management:** Greenbone Community Edition
- **Live Response:** Velociraptor — artifact collection and hunting
- **Network:** Suricata IDS/IPS on OPNsense

---

## Certification Path

OSCP → OSEP → OSWE → OSED → OSCE3 → GCIA → GCFA → GCTI → GMON → CISSP → SABSA → CCSP

---

## Repository Structure

| Repo | Contents |
|------|----------|
| [osim-core](https://github.com/osim-framework/osim-core) | Lab runbooks, incident reports, architecture docs |
| [osim-framework](https://github.com/osim-framework/osim-framework) | Framework specification and whitepaper |

---

## Documentation

- `OSIM_Portfolio.pdf` — Complete framework specification
- `osim-core/runbooks/` — Lab build sheets and deployment guides
- `osim-core/incidents/` — Incident reports and post-mortems

---

## Contact

**LinkedIn:** [linkedin.com/in/alec-s81243565](https://linkedin.com/in/alec-s81243565)  
**GitHub:** [github.com/osim-framework](https://github.com/osim-framework)
