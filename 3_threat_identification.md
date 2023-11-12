# 3_threat_identification

## **3.1. Threat Taxonomy for Log Data**

The [MITRE ATT&CK Matrix](https://attack.mitre.org/) provides a proven resource for an overview of attacks that log sources can embed.

<details>
  <summary><strong>Threat Taxonomy for Log Data</strong></summary>

  | Category | Description | Examples |
  | --- | --- | --- |
  | Access Control | Threats related to authentication, authorization, and session management. | Excessive Role Granted, Unusual Logon Times, Multiple Logon Failures, Geographically Improbable Login, Unauthorized Cloud Database Access |
  | Data Movement | Threats related to the movement, transfer, and sharing of data. | Data Export Activity, Abnormal Data Transfer, Suspicious File Uploads, Data Exfiltration, Unexpected Data Retrieval |
  | Configuration Issues | Threats arising from misconfigurations in software, services, or infrastructure. | Public Storage System Exposure, Log Configuration Changes, Cloud Resource Misconfiguration, Insecure Network Exposure, Misconfigured Identity Policies |
  | Network Anomalies | Threats related to unusual or unauthorized network traffic patterns and sources. | Suspicious Network Traffic Patterns, Suspicious Outbound Connections, Elevated Network Traffic, Infiltration of Security Groups, Suspicious DNS Queries |
  | Resource Misuse | Threats arising from the misuse of cloud or organizational resources. | Unexpected Resource Creation, Cloud Service Scaling Anomalies, Unauthorized Application Installation, Misuse of Cloud Storage APIs, Unauthorized Cloud Service Deployment |
  | API and Service Abuse | Threats related to the misuse or abuse of APIs and other platform-specific services. | API Token Abuse, Service Misuse, Unauthorized Cloud API Exposure, Malicious Code Execution, Third-party Integration Anomalies |
  | Information Exposure | Threats related to the unintended exposure or leakage of sensitive or critical information. | Sensitive Data Exposure, External Document Sharing, Cloud Credential Abuse, Information Disclosure, API Data Leak |
  | Operational Anomalies | Threats related to operational aspects of cloud platforms or infrastructure. | Cloud Billing Anomalies, Infrastructure Drift, Unauthorized Cloud API Exposure, Log Configuration Changes, Unexpected Admin Activity |
  | Insider Threats | Threats originating from within the organization, including accidental or intentional actions. | Misuse of Resources, Data Theft by Employees, Inappropriate Access or Data Retrieval, Insider-driven Configuration Changes |
  | Physical Threats | Threats concerning the physical security of infrastructure, including data centers and hardware. | Theft of Hardware, Sabotage of Infrastructure, Natural Disasters Affecting Operation, Physical Infiltration of Data Centers |
  | Third-party Risks | Threats arising from third-party integrations, vendors, and other external entities. | Vulnerable Third-party Software, Supply Chain Attacks, Partner Data Leaks, Unauthorized Third-party Data Access, Compromised Third-party Applications |
  | Code Execution | Threats related to the execution of malicious or unauthorized code. | Remote Code Execution, Script Injection Attacks, Malware Execution, Unauthorized Cloud Function Triggers |
  | Social Engineering | Threats leveraging human factors to gain unauthorized access, manipulate individuals, or steal data. | Phishing Attacks, Spear Phishing, Whaling, Vishing, Baiting, Pretexting, Tailgating |

</details>


---

## **3.2. Threat Origins**

By allocating sources of threats to discerned threat categories and enabling detection engineers to create threat personas based on this foundation for detection rules, we enhance the precision and relevance of our security measures through a deeper understanding of these origins.

| Threat Origin | Description |
| --- | --- |
| External | Threats originating outside the organization |
| Internal | Threats from disgruntled employees or insiders |
| Partners | Threats due to third-party integrations or vendors |



<details>
  <summary><strong>Threat Sources</strong></summary>

  | Threat Source | Description |
  | --- | --- |
  | Supply Chain | Threats arising from the entire supply chain, encompassing hardware manufacturers, software developers, and service providers. A compromised component can introduce vulnerabilities into the end product or service. |
  | Customers/Clients | In platforms with user-generated content or customizability, customers might inadvertently (or intentionally) introduce security vulnerabilities. |
  | Contractors and Consultants | Unlike regular employees, these individuals might not be fully versed in a company's security culture. With temporary access to resources, they could inadvertently introduce threats. |
  | Automated or Bots | Automated scripts, crawlers, or bots programmed to exploit vulnerabilities, perform DDoS attacks, or scrape information. These are specifically non-human and automated threats. |
  | Competitors | In corporate espionage scenarios, competitors might try to infiltrate, disrupt, or steal information. |
  | State-sponsored Actors | Groups backed by nation-states or governments with motives ranging from espionage to cyber warfare. |
  | Hacktivists | Groups or individuals executing cyber-attacks based on political or ideological motives. |
  | Former Employees | Those who have left an organization but might still have access or could harbor grievances motivating malicious actions. |
  | Physical Intruders | Individuals bypassing digital security by exploiting physical vulnerabilities to gain access to facilities. |
  | Cloud Service Providers | Trusted with data and services, there's a risk these providers might be compromised or might inadvertently expose data. |
  | Current Employees (Insider Threats) | Employees within the organization might misuse their access due to various motives, such as financial gain, curiosity, or grievances. They could intentionally or unintentionally become a threat. |
  | Third-party Vendors | Organizations or individuals who provide services or products to your organization but aren't directly employed by you. They might have some level of access to your systems or data, presenting a potential threat vector. |

</details>
