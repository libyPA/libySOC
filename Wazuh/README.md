# Wazuh SOC Monitoring & Incident Response

## Overview

This project documents a hands-on SOC monitoring lab built using **Wazuh** to detect, investigate, and respond to simulated security activity in a controlled virtual environment.

The lab focuses on the workflow followed by a SOC analyst:

**Security Event → Log Collection → Detection → Alert Investigation → MITRE ATT&CK Mapping → Response & Containment**

---

## 🏗️ Lab Architecture

```text
                    Simulated Attacker
                           │
                           │
                    Security Activity
                           │
                           ▼
                ┌─────────────────────┐
                │   Ubuntu / DVWA     │
                │                     │
                │ Apache + PHP + DVWA │
                │ auditd              │
                │ Wazuh Agent         │
                └──────────┬──────────┘
                           │
                           │ Security Telemetry
                           ▼
                ┌─────────────────────┐
                │   Wazuh Manager     │
                │                     │
                │ Log Analysis        │
                │ Detection Rules     │
                │ Alert Generation    │
                │ MITRE Mapping       │
                │ Active Response     │
                └──────────┬──────────┘
                           │
                           ▼
                  Investigation &
                     Containment
```

---

## 🔍 Objectives

* Deploy and configure a Wazuh monitoring environment.
* Monitor security events from a Linux web server.
* Collect and analyze Apache and auditd telemetry.
* Create custom Wazuh detection rules.
* Investigate generated security alerts.
* Map detected activity to MITRE ATT&CK techniques.
* Implement Wazuh Active Response for automated containment.
* Document the investigation and response workflow.

---

## 🛠️ Technologies Used

* Wazuh
* Linux / Ubuntu
* Apache
* PHP
* DVWA
* auditd
* MITRE ATT&CK
* VirtualBox

---

## 🧪 Security Activity

The lab generated controlled security activity against the DVWA environment to test detection and response capabilities.

Activities included simulated:

* Web application attacks
* File inclusion activity
* Suspicious file activity
* Authentication-related activity
* Command execution activity

All testing was performed within an isolated lab environment.

---

## 🚨 Detection Engineering

Custom Wazuh rules were created to identify suspicious activity that was not adequately covered by the default monitoring configuration.

The rules were designed to:

1. Identify relevant security events.
2. Generate Wazuh alerts.
3. Provide useful event context for investigation.
4. Associate relevant activity with MITRE ATT&CK techniques.
5. Trigger response actions where appropriate.

---

## 🕵️ Alert Investigation

For detected events, the investigation process included:

* Reviewing Wazuh alerts.
* Examining the associated log entries.
* Identifying the source and nature of the activity.
* Reviewing Apache and auditd telemetry.
* Extracting relevant indicators.
* Determining whether the activity represented suspicious or malicious behavior.
* Correlating events to understand the attack sequence.

---

## 🗺️ MITRE ATT&CK Mapping

Relevant detected activity was mapped to the **MITRE ATT&CK framework** to provide standardized classification of adversary behavior.

The mapping was used to understand:

* Initial access or attack vector
* Execution activity
* Persistence or follow-on activity where applicable
* Relevant discovery or system activity
* Impact or containment considerations

The exact technique mapping is documented alongside the individual detection rules and investigations.

---

## 🛡️ Active Response & Containment

Wazuh Active Response was configured to demonstrate automated host-level containment.

The response workflow was:

```text
Suspicious Activity
        │
        ▼
Wazuh Detection Rule
        │
        ▼
Security Alert
        │
        ▼
Active Response Trigger
        │
        ▼
Host-Level Blocking
        │
        ▼
Containment
```

This demonstrates how a SOC monitoring platform can move beyond detection and support automated response to security events.

---

## 📊 SOC Investigation Workflow

```text
1. Monitor
      ↓
2. Detect
      ↓
3. Triage
      ↓
4. Investigate
      ↓
5. Identify Indicators
      ↓
6. Map to MITRE ATT&CK
      ↓
7. Respond
      ↓
8. Contain
      ↓
9. Document
```

---

## 📁 Project Documentation

Detailed documentation will be added to this project covering:

* Lab setup
* Wazuh agent configuration
* Detection rules
* Alert investigation
* MITRE ATT&CK mapping
* Active Response configuration
* Containment workflow
* Investigation findings

---

## ⚠️ Disclaimer

This project was performed in a controlled cybersecurity lab environment for educational and portfolio purposes.

No testing was performed against systems without authorization.
