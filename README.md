# SOC-Automation-Lab
A home SOC lab using Wazuh and Shuffle to monitor Windows security events and automate alerts.

# SOC Automation Lab

A home SOC automation lab built using **Wazuh** and **Shuffle SOAR**.

The project monitors security events from a Windows 11 machine using Wazuh and Sysmon, then sends the alerts to Shuffle for automated processing and email notification.

## Architecture

```text
Windows 11
   │
   ├── Sysmon
   └── Wazuh Agent
          │
          ▼
   Wazuh Manager
          │
          ▼
   Wazuh Indexer
          │
          ▼
   Wazuh Dashboard
          │
          ▼
   Shuffle SOAR
          │
          ▼
   Email Alert
```

## Technologies

- Wazuh
- Shuffle SOAR
- Sysmon
- Windows 11
- Ubuntu Server
- Docker
- VirtualBox

## What I Built

- Set up a Wazuh SIEM environment on Ubuntu Server.
- Connected a Windows 11 host to Wazuh using the Wazuh Agent.
- Configured Sysmon to collect Windows security events.
- Monitored and analyzed Windows activity through the Wazuh Dashboard.
- Installed Shuffle SOAR in a separate Ubuntu Server VM.
- Integrated Wazuh alerts with a Shuffle webhook.
- Created a Shuffle workflow that receives Wazuh alerts and sends email notifications automatically.

## Workflow

```text
Wazuh Alert
     ↓
Shuffle Webhook
     ↓
Send Email
     ↓
Email Notification
```

## Example

For testing, Windows security activity was generated on the monitored machine and detected by Wazuh.

The alert was then sent to Shuffle through the webhook, where the workflow processed the alert and sent an email notification.

## Project Status

Completed as a basic SOC automation lab.

The project currently focuses on **Wazuh alert detection, Shuffle integration, and automated email notification**.

Possible future extensions include:

- IOC enrichment with VirusTotal
- Severity-based alert routing
- Automated incident records
- Additional notification channels
- Safe automated response actions

## Notes

This project was built as a learning and portfolio project to gain practical experience with SIEM, SOAR, security monitoring, and security alert automation.

No real production systems were used for testing.
