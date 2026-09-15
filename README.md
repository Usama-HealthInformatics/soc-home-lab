# SOC Home Lab

A practical defensive security operations project focused on security monitoring, log analysis, alert investigation, detection engineering, and incident response.

## Objectives

* Understand Security Operations Center workflows
* Analyze security-relevant logs
* Investigate suspicious activity
* Develop basic detection logic
* Document security alerts and findings
* Practice incident-response methodology
* Understand SIEM and security-monitoring concepts

## SOC Workflow

```text
Log Sources
     ↓
Log Collection
     ↓
Normalization
     ↓
Detection Rules
     ↓
Security Alert
     ↓
Analyst Investigation
     ↓
Incident Classification
     ↓
Response & Remediation
     ↓
Lessons Learned
```
## Project Areas

### SOC Workflow

A documented security operations workflow from log collection through incident response.

### Failed Login Investigation

A simulated investigation of repeated authentication failures, including triage, analysis, risk assessment, and response.

### Detection Engineering

A documented detection rule for repeated failed authentication activity.

### Incident Response

An authentication-security incident-response playbook covering identification, triage, investigation, containment, eradication, recovery, and lessons learned.## Project Areas

### Security Monitoring

Review security events and identify activity that may require investigation.

### Log Analysis

Analyze authentication, system, network, and security events to identify suspicious behavior.

### Alert Investigation

Evaluate security alerts and determine whether activity is:

* Benign
* Suspicious
* Malicious
* False positive

### Detection Engineering

Develop simple detection logic for common security events such as:

* Multiple failed logins
* Suspicious authentication activity
* Unusual network connections
* Privilege escalation indicators
* Potential malware activity

### Incident Response

Use a structured process:

1. Identification
2. Triage
3. Investigation
4. Containment
5. Eradication
6. Recovery
7. Lessons learned

## Tools & Technologies

* SIEM concepts
* Security event logs
* Windows Event Logs
* Linux security logs
* Network security logs
* Detection rules
* Incident-response frameworks
* GitHub documentation

## Security Scope

All security investigations and testing should be performed only on systems and data that are owned by the researcher or explicitly authorized for analysis.

## Repository Structure

```text
soc-home-lab/
├── README.md
├── documentation/
├── detections/
├── investigations/
├── incident-response/
└── reports/
```
## Status

**Completed — Documentation-Based SOC Operations Lab**

The project documents a complete defensive SOC workflow covering security monitoring, log analysis, alert investigation, detection engineering, and incident response.

The scenarios are explicitly documented as simulated training exercises and do not claim access to production systems or unauthorized environments.
