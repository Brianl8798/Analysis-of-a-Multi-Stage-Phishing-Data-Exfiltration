# Multi-Stage Phishing Data Exfiltration : KQL Incident Investigation

<p align="center">
  A full incident response investigation into a multi-vector phishing campaign, hunting through logs with KQL in a controlled cyber range.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/KQL-Threat_Hunting-red" alt="KQL">
  <img src="https://img.shields.io/badge/Azure_Data_Explorer-0078D4?logo=microsoftazure&logoColor=white" alt="Azure Data Explorer">
  <img src="https://img.shields.io/badge/MITRE-ATT%26CK-C8102E" alt="MITRE ATT&CK">
  <img src="https://img.shields.io/badge/Windows_10-21H2-0078D6?logo=windows&logoColor=white" alt="Windows 10 21H2">
</p>

> [!TIP]
> **Want to see the queries in action?** Jump to [Screenshots](#screenshots).
>
> - 🎣 Investigated a **multi-stage phishing** campaign from first email to data exfiltration
> - 🔎 Pivoted across logs by **timestamp, IP, username, URL and role**
> - 🗺️ Attributed adversary TTPs to **MITRE ATT&CK**
> - 🛡️ Produced **actionable countermeasures**

## Table of Contents

- [Introduction](#introduction)
- [Objectives](#objectives)
- [Tools & environment](#tools--environment)
- [Investigation approach](#investigation-approach)
- [Screenshots](#screenshots)
- [Credits](#credits)

## Introduction

This project executes a **full incident response lifecycle**: investigating a multi-vector phishing campaign inside a controlled cyber range, analyzing system and application logs, and tracing the attacker from initial contact through to data exfiltration.

## Objectives

- Investigate a **multi-vector phishing campaign** end to end
- Analyze **system and application logs** to reconstruct attacker activity
- Attribute adversary TTPs to the **MITRE ATT&CK®** framework
- Engineer **definitive, actionable countermeasures**

## Tools & environment

| Category | Details |
| --- | --- |
| Query language | KQL (Kusto Query Language) |
| Platform | Azure Data Explorer |
| Environment | Windows 10 (21H2) |

## Investigation approach

Each stage of the investigation started from one known indicator and **pivoted** to the next:

1. **Scope by time** — filter logs to the window around the first suspicious event
2. **Pivot on IP** — find every record tied to the attacker's IP address
3. **Pivot on identity & URLs** — connect usernames, visited URLs and IPs to map who was targeted and what was clicked
4. **Pivot on role** — query by employee role to find which groups the campaign focused on

## Screenshots

**KQL searches for logs by timestamp, IP or text**

![KQL search by timestamp, IP or text](https://github.com/user-attachments/assets/92f61bdd-3913-4a51-9558-b24d6251a1b8)

**Results of a KQL search for a specific IP**

![KQL search results for a specific IP](https://github.com/user-attachments/assets/a6351d5c-e7f6-4470-9f8a-68dd80d63d86)

**Additional KQL search involving username, URLs and IP**

![KQL search involving username, URLs and IP](https://github.com/user-attachments/assets/300bcc20-bc94-403e-a47d-84b52c011f8b)

**Results of a KQL search for the role "rapper"**

![KQL search results for the role rapper](https://github.com/user-attachments/assets/d6103199-445d-4aac-b1ad-827a55ac57c6)

## Credits

- Brian Lam — [GitHub](https://github.com/Brianl8798) · [LinkedIn](https://www.linkedin.com/in/brian-lam-282176172/)
