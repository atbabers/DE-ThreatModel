# 1_log_source_characterization

## **1.1. Characterize Log Source**

To use log data for detection engineering, it’s crucial to understand the log source. To do this, we need to examine the source, its data, and how it fits into the organization's ecosystem. We can leverage existing log source categorizations by [Google Chronicle](https://cloud.google.com/chronicle/docs/ingestion/parser-list/supported-default-parsers).

<details>
  <summary>Log Source Character Types</summary>

  | Log Type | Threat Detection Use Case | Examples |
  | --- | --- | --- |
  | Asset Management (Axonius, JupiterOne) | Unauthorized Asset Changes | Modifications to asset records or new devices without proper categorization. |
  | Identity Management (Okta) | Brute Force Attempts | Multiple failed login attempts from the same IP or user. |
  | BI Tools (Tableau, Power BI) | Data Export Anomalies | Exporting large datasets or accessing sensitive reports. |
  | CDN Services (Akamai, CDN77) | Traffic Diversion | Redirecting traffic to suspicious domains or unexpected traffic drops. |
  | Cloud Storage (Dropbox, Box) | Unusual Data Downloads | Bulk data downloads or access from unrecognized devices. |
  | Collaboration Tools (Trello, Notion) | Irregular Board Changes | Deletion of critical boards or unauthorized task assignments. |
  | Communication Platforms (Twilio, Signal) | Suspicious Communication Patterns | Unusual spikes in messages or calls to high-risk regions. |
  | Container Orchestration (Kubernetes, Docker) | Misconfigured Deployments | Exposed services or unusual container behaviors. |
  | Customer Support (Zendesk) | Unauthorized Ticket Access | Accessing tickets not assigned or data export patterns. |
  | Database Activity Logs | Excessive Queries | High frequency of SELECT statements from one user. |
  | Development Tools (Snyk) | Vulnerability Detections | Introduction of new code vulnerabilities or outdated libraries. |
  | DNS Logs | Domain Generation Algorithms (DGA) | Requests to random or algorithmically generated domains. |
  | Email Logs | Phishing Campaigns | Emails with malicious attachments or links. |
  | Endpoint Logs | Malware Infection | Sudden spike in disk activity or unusual process execution. |
  | Endpoint Security (Crowdstrike, SentinelOne) | Threat Prevention Failures | Disabling of security tools or detection bypass attempts. |
  | Fleet Management Systems | Unauthorized Vehicle Access | Vehicles moving during non-operational hours or route deviations. |
  | Industrial Control Systems | Machine Behavior Anomalies | Unusual machine startups or unexpected configuration changes. |
  | Integration Platforms (Fluentd, Tines) | Integration Failures | High rate of failed data integrations or unexpected source integrations. |
  | IoT Devices | Unauthorized Device Access | Sudden change in device configurations or unexpected outbound traffic. |
  | Mobile Device Management (MDM) | Lost/Stolen Device | Multiple failed unlock attempts or device not checking in. |
  | Network (AWS VPC Flow Logs) | Port Scanning | Numerous requests to various ports from one IP. |
  | Password Managers (1Password, Bitwarden) | Vault Access Anomalies | Multiple incorrect password entries or new device logins. |
  | Physical Security Systems (Camera, Entry Logs) | Unauthorized Physical Access | Entry during off-hours or unrecognized badge scans. |
  | POS Systems (Square, Verifone) | Fraudulent Transactions | Multiple transactions from the same card in short time intervals. |
  | Real-time Communication (WhatsApp, Telegram) | Suspicious Message Patterns | Rapid message deletions or transmission of large files. |

</details>

### **1.1.1 Determine Data Categories**

- **Type of Data**: Start by identifying the primary purpose of the log source. Does it log authentication events, system processes, user transactions, network traffic, or something else?
- **Granularity**: Understand the level of detail the logs capture. For instance, does a network log capture packet-level data, or is it more high-level, tracking only connection events?
- **Volume**: Estimate the volume of log entries generated within a specific time frame (e.g. daily). This can give insights into the storage and processing resources required.

### **1.1.2 Identify Connectivity**

- **Associated Systems**: Determine which systems or applications generate the logs. For instance, is it a web server, database system, firewall, or a user authentication portal?
- **Interdependencies**: Understand if the log source has dependencies on other systems. For example, does an application server log source also interact with a database or an authentication service?
- **External Interactions**: Check if the log source captures interactions with external entities. For instance, does a firewall log show incoming connections from external IP addresses?

### **1.1.3 Know the Stakeholders**

- **Primary Users**: Identify the primary users or user groups associated with the log source. For a database, this might be database administrators and regular users.
- **Administrative Personnel**: Determine who has administrative or elevated privileges on the system. These individuals might have more sensitive log entries or specific types of events associated with their actions.

### **1.1.4 Historical Context**

- **Log Retention**: Understand how long the logs are retained and if there’s a rotation or archival policy in place.
- **Past Incidents**: Review past security incidents or anomalies associated with this log source. Historical context can provide insights into patterns to watch out for or specific vulnerabilities of the system.
- **SIEM Integration**:
    - **SIEM Integration**: Check if we integrate the logs with a Security Information and Event Management (SIEM) system or any other centralized log management solution.
    - **Alert Configurations**: Understand if there are any pre-existing alert configurations associated with this log source, which can provide clues about critical events or