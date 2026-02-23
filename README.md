# 🛡️ Home SOC Lab — Brute Force Detection with Elastic SIEM

## Overview
A fully functional Home SOC Lab built using the ELK Stack (Elastic 8.15.2) 
running in Docker on macOS. This project demonstrates real-time threat 
detection, SIEM log analysis, and formal incident documentation.

## Lab Architecture
target-node (Ubuntu 22.04)
   └── Filebeat
         └──► Logstash :5044
                  └──► Elasticsearch :9200
                              └──► Kibana :5601

## What Was Detected
- **Attack Type:** Brute Force SSH Login Attempts
- **MITRE ATT&CK:** T1110 — Brute Force / Credential Access (TA0006)
- **Events Detected:** 3 confirmed failed authentication events
- **Total Events Indexed:** 4,706 (filebeat-2026.02.20)
- **Detection Method:** KQL query — `message: "Failed password"`

## Tools Used
| Tool | Version | Purpose |
|---|---|---|
| Elasticsearch | 8.15.2 | Log storage and indexing |
| Logstash | 8.15.2 | Log processing pipeline |
| Kibana | 8.15.2 | SIEM visualisation |
| Filebeat | 8.19.11 | Log shipping agent |
| Docker | Latest | Container orchestration |
| Ubuntu | 22.04 (ARM64) | Target and control nodes |

## Project Deliverables
- ✅ Working SIEM pipeline (Filebeat → Logstash → Elasticsearch → Kibana)
- ✅ Brute force attack simulation and detection
- ✅ SOC Dashboard with 3 visualisations
- ✅ MITRE ATT&CK T1110 mapped detection rule in Elastic SIEM
- ✅ Professional Incident Report (see PDF below)

## 📄 Incident Report
Check SOC_Incident_Report_v2.pdf file for incident report.

## Screenshots
Kibana screenshots (dashboard, discover, MITRE ATT&CK)

## Analyst
**Aruna Kottilingalthode**  
CompTIA Security+ | CompTIA A+  
MSIT Cybersecurity Programme  
linkedin.com/in/arunaksvv
