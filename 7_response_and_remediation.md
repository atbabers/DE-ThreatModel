# 7_response_and_remediation

## 7.1. Developing Response & Remediation Strategies

**For each identified threat, develop a strategy:**

1. **Detection** - Identify signs of the threat in the logs.
2. **Response** - Define procedures to respond when a threat is detected.
3. **Remediation** - Determine actions to prevent the threat from recurring.

<details>
  <summary><strong>Response and Remediation Strategies</strong></summary>

  | Threat | Detection Indicators | Response Action | Remediation Steps |
  | --- | --- | --- | --- |
  | Malware | Unusual system behavior, File changes | Isolate affected system | Update antivirus, Patch vulnerabilities |
  | Phishing | Suspicious email patterns, Unusual login locations | Inform affected users | Update email filters, Train employees |
  | Public Storage System Exposure | Unauthorized access logs, Public accessibility flags | Restrict access, Notify admins | Review and update storage configurations |
  | API Token Abuse | Unusual API call patterns, Unauthorized access logs | Revoke abused token, Notify admins | Rotate API tokens regularly, Monitor API usage |
  | External Document Sharing | Unusual sharing patterns, Sharing outside domain logs | Restrict sharing, Notify affected users | Implement sharing policies, Train users |
  | Unusual Logon Times | Logins during off-hours, Multiple logins from different locations | Notify affected users, Review account | Update account security policies, Train employees |
  | Multiple Logon Failures | Consecutive failed login attempts | Lock account, Notify affected user | Implement CAPTCHA or multi-factor authentication |
  | Data Export Activity | Large data transfer logs, Unusual export patterns | Monitor and restrict exports, Notify admins | Implement DLP solutions |
  | New Source Application Access | Unrecognized device logs, Unfamiliar IP address logs | Alert admin, Review access logs | Implement geo-fencing or IP whitelisting |
  | Log Configuration Changes | Changes to logging settings, Unexpected configuration changes | Restore default settings, Notify admins | Review and audit log configurations regularly |
  | Geographically Improbable Login | Logins from distant locations in short time frames | Alert user and admin, Review account activity | Implement geo-based anomaly detection |
  | Unauthorized Cloud Database Access | Unauthorized query logs, Unusual access patterns | Lock down database, Notify admins | Strengthen database authentication and access controls |
  | Malicious Code Execution | Unexpected system behavior, Altered application logs | Isolate affected application or system | Patch application vulnerabilities, Monitor code execution |
  | Misuse of Cloud Storage APIs | Abnormal API call logs, Unauthorized access attempts | Restrict API access, Notify admins | Monitor and restrict certain API calls |
  | Suspicious Network Traffic Patterns | Unusual traffic volume, Unexpected communication to known malicious IPs | Monitor and possibly restrict traffic, Notify network admins | Implement network segmentation and intrusion detection systems |
  | Unexpected Admin Activity | Logs of unexpected administrative actions, Changes without documentation | Revert changes, Notify higher management | Regularly review admin logs, Update admin authentication protocols |
  | Cloud Resource Misconfiguration | Exposure logs, Configuration change logs without associated approvals | Revert to secure configuration, Notify cloud admins | Regularly audit and review cloud configurations |
  | Suspicious DNS Queries | Queries to known malicious domains, High volume of subdomain queries | Restrict DNS queries, Notify network admins | Implement DNS monitoring and filtering |
  | Unauthorized Cloud API Exposure | Logs of public API access, Unexpected API calls | Restrict API exposure, Notify cloud admins | Regularly review and update API access controls |
  | Anomalous Resource Deletion | Unexpected deletion logs, Resource unavailability | Restore from backups, Notify admins | Implement stricter resource deletion policies |
  | Cloud Credential Abuse | Unusual activity from a known user, Multiple resource accesses in short time | Reset credentials, Notify affected user and admins | Rotate and audit cloud credentials regularly |
  | Suspicious Outbound Connections | Traffic to known malicious IPs, Large data transfers to unfamiliar IPs | Restrict outbound connections, Notify network admins | Review and update firewall and egress rules |
  | Insecure Cloud Service Defaults | Services deployed with open permissions, Public access logs | Restrict service permissions, Notify cloud admins | Regularly review cloud service configurations, Implement security policies |
</details>
