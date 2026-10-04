# Splunk SIEM Monitoring & Web Attack Investigation

## Overview

Hands-on Splunk SIEM lab focused on **security monitoring, log analysis, and investigation of simulated web application attacks** in a controlled environment.

## Objectives

* Centralize Windows and Linux security telemetry in Splunk.
* Use SPL to search and investigate security events.
* Analyze simulated web attacks against DVWA.
* Identify suspicious activity and relevant IOCs.
* Practice a structured SOC investigation workflow.

## Technologies

* Splunk Enterprise
* Splunk Universal Forwarder
* SPL
* Windows
* Linux / Ubuntu
* Sysmon
* Apache
* auditd
* DVWA

## Investigation Focus

The project includes investigation of:

* Local File Inclusion (LFI)
* Remote File Inclusion (RFI)
* Authentication-related activity
* Suspicious HTTP requests
* Web attack indicators

The investigation involved analyzing Apache logs, HTTP requests, response codes, request patterns, and response sizes to determine attack activity.

## Project Documentation

Detailed implementation, investigation findings, and lab architecture are available in the project documentation.

* **Lab & Investigation Documentation** → `documentation/`
* **Architecture** → `documentation/`

## Disclaimer

This project was performed in a controlled cybersecurity lab environment for educational and portfolio purposes.
