# Hi, I'm Abdelrahman Elzein 👋

### SOC Analyst | SIEM | DFIR | Network Security

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/abdelrahman-elzein)

---

## 👨‍💻 About Me

Cybersecurity professional with a background in Network and Security Engineering and hands-on SOC/DFIR training.

- 1.4 years of professional experience in Network & Security Engineering.
- 10 months of intensive, hands-on SOC & DFIR training.
- Practical experience with SIEM deployment, security monitoring, alert triage, and threat hunting.
- Hands-on exposure to digital forensics, attack-chain reconstruction, and AWS cloud investigations.
- Interested in Security Operations, Incident Response, Threat Detection, and Digital Forensics.

Currently focused on developing practical SOC investigation, detection engineering, and SOAR automation skills.

---

## 🛠️ Technical Skills

| Category | Technologies & Skills |
|---|---|
| SIEM & Security Analytics | Wazuh, Splunk, Elastic Stack, IBM QRadar |
| Detection & Investigation | SPL, KQL, Alert Triage, Threat Hunting, IOC Analysis |
| EDR/XDR | LimaCharlie, Microsoft Defender XDR |
| SOAR & Incident Management | Tines, Shuffle, TheHive |
| Cloud Investigation | AWS CloudTrail, IAM, S3, EC2 |
| Digital Forensics | FTK Imager, Volatility 3, Autopsy, KAPE, EZParser |
| Network Security | FortiGate, Palo Alto, Cisco FTD/FMC, Cisco ISE |
| Operating Systems & Logging | Windows, Linux, Sysmon, Auditd |

---

## 💻 Tools & Technologies

### SIEM & Security Analytics

![Wazuh](https://img.shields.io/badge/Wazuh-SIEM%2FXDR-4A90E2?style=for-the-badge)
![Splunk](https://img.shields.io/badge/Splunk-000000?style=for-the-badge&logo=splunk&logoColor=white)
![Elastic](https://img.shields.io/badge/Elastic_Stack-005571?style=for-the-badge&logo=elastic&logoColor=white)
![IBM QRadar](https://img.shields.io/badge/IBM_QRadar-052FAD?style=for-the-badge&logo=ibm&logoColor=white)

### EDR & Detection

![LimaCharlie](https://img.shields.io/badge/LimaCharlie-333333?style=for-the-badge)
![Microsoft Defender](https://img.shields.io/badge/Microsoft_Defender_XDR-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)

### SOAR & Incident Management

![Tines](https://img.shields.io/badge/Tines-SOAR-5A45FF?style=for-the-badge)
![Shuffle](https://img.shields.io/badge/Shuffle-SOAR-6C4AB6?style=for-the-badge)
![TheHive](https://img.shields.io/badge/TheHive-Incident_Management-F1A33C?style=for-the-badge)

### Digital Forensics & Incident Response

![FTK Imager](https://img.shields.io/badge/FTK_Imager-444444?style=for-the-badge)
![Volatility](https://img.shields.io/badge/Volatility_3-444444?style=for-the-badge)
![Autopsy](https://img.shields.io/badge/Autopsy-444444?style=for-the-badge)
![KAPE](https://img.shields.io/badge/KAPE-444444?style=for-the-badge)
![EZParser](https://img.shields.io/badge/EZParser-444444?style=for-the-badge)

### Cloud Security & Investigation

![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![CloudTrail](https://img.shields.io/badge/AWS_CloudTrail-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![IAM](https://img.shields.io/badge/AWS_IAM-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![EC2](https://img.shields.io/badge/Amazon_EC2-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![S3](https://img.shields.io/badge/Amazon_S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white)

### Network Security

![Fortinet](https://img.shields.io/badge/Fortinet-EE3124?style=for-the-badge&logo=fortinet&logoColor=white)
![Palo Alto](https://img.shields.io/badge/Palo_Alto_Networks-F04E23?style=for-the-badge)
![Cisco](https://img.shields.io/badge/Cisco-049FD9?style=for-the-badge&logo=cisco&logoColor=white)

---

## 🚀 Projects

### LimaCharlie + Tines SOAR – Automated Endpoint Isolation

A hands-on SOAR automation lab integrating LimaCharlie EDR, Tines Stories, Slack, email notifications, and a Windows 10 endpoint.

**Implementation:**
- Created and tested a LimaCharlie detection rule to identify LaZagne.exe execution.
- Configured LimaCharlie to forward security detections to Tines through a webhook.
- Integrated Slack and email notifications for security alerts.
- Implemented a human approval mechanism before endpoint isolation.
- Automated endpoint isolation through LimaCharlie following analyst approval.
- Implemented separate approval and rejection workflows.
- Retrieved and verified the endpoint's isolation status.

**Technologies:** LimaCharlie EDR (D&R Rules/YAML), Tines Stories, Slack, Windows 10, Webhooks, REST API.

[![View Project](https://img.shields.io/badge/View_Project-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Abdelrahman-Elzein/LimaCharlie-Tines-SOAR-EDR-Automation)

### Wazuh + TheHive + Shuffle SOAR – Automated Mimikatz Detection & Endpoint Isolation

A hands-on SOAR automation lab integrating Wazuh SIEM/XDR, Shuffle SOAR, TheHive, VirusTotal threat intelligence, and a Windows 10 endpoint.

**Implementation:**
- Deployed and configured Wazuh Manager and a Windows 10 agent, integrating Sysmon telemetry and enabling raw event archiving for custom detection development.
- Developed a custom Wazuh detection rule using PE `originalFileName` metadata to detect Mimikatz execution, including renamed binaries, mapped to MITRE ATT&CK technique T1003.
- Integrated Wazuh security alerts with Shuffle through a webhook and automated SHA-256 hash extraction from Sysmon telemetry.
- Integrated VirusTotal's API to retrieve malware reputation and analysis information using the extracted SHA-256 hash.
- Configured a local Shuffle Orborus worker to communicate with the self-hosted Wazuh and TheHive infrastructure.
- Automated email notifications containing relevant incident details, endpoint telemetry, and the extracted malware hash.
- Automated TheHive alert creation with enriched incident details, including affected host information, process metadata, and file hashes.
- Triggered Wazuh Active Response to automatically isolate the compromised Windows endpoint using Windows Firewall.
- Validated the complete workflow by executing a renamed Mimikatz binary, verifying detection, notification, alert creation, endpoint isolation, and subsequent manual recovery.

**Technologies:** Wazuh 4.12, Sysmon, Shuffle SOAR, TheHive, Windows 10, Windows Firewall, Webhooks, REST API.

[![View Project](https://img.shields.io/badge/View_Project-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Abdelrahman-Elzein/Wazuh-TheHive-Shuffle-SOAR-Automation)

---

## 🧪 Hands-on Training & Labs

Practical SOC, SIEM, threat-hunting, cloud investigation, and DFIR exercises completed through structured training and lab environments.

- **TryHackMe SOC Level 1:** Completed the SOC Level 1 learning path.
- **SOC Simulations:** Practised security alert investigation, True/False Positive classification, attack-chain reconstruction, escalation decisions, and incident reporting.
- **SIEM Labs:** Deployed and configured Splunk Enterprise, Elastic Stack, IBM QRadar CE, and Wazuh; integrated Windows, Sysmon, Linux, and application telemetry; developed and tested detection rules.
- **AWS Security Investigations:** Investigated simulated cloud-security incidents using CloudTrail, IAM, S3, and EC2.
- **DFIR Exercises:** Practised forensic disk acquisition, memory analysis, and Windows artifact collection using FTK Imager, Volatility 3, Autopsy, KAPE, and EZParser.
- **Microsoft Defender XDR:** Completed Microsoft Defender for Endpoint training and hands-on investigation exercises.

---

## 🎓 Certifications

- Red Hat Certified System Administrator (RHCSA)
- Cisco CCNP Security
- Cisco CCNP Enterprise
- Cisco CCNA
- Cisco ENARSI
- Cisco ENCOR
- Cisco SCOR
- Cisco SNCF
- VMware VCP-DCV

### Additional Courses & Training

- SOC & DFIR Specialist Training – RaiseUp Learning
- TryHackMe SOC Level 1
- CHFI
- CEH
- Splunk
- IBM QRadar
- Elastic Stack (ELK)
- Microsoft Defender for Endpoint (MDE)
- Microsoft Defender XDR
- PCNSE, NSE4, MCSA, Cisco Meraki, and ENWLSI

---

## 🌍 Additional Information

- 📍 Cairo, Egypt
- 🌐 Open to relocation
- 🗣️ Arabic (Native) | English (Full Professional Proficiency)

---

## 📫 Connect With Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Abdelrahman_Elzein-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/abdelrahman-elzein)
