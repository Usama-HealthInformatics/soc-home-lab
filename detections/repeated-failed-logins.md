# Detection Rule — Repeated Failed Logins

## Purpose

Detect repeated authentication failures that may indicate credential attacks, password spraying, brute-force activity, or account misuse.

This is a **defensive detection design** intended for a SOC environment.

## Detection Logic

```text id="w9d2nf"
IF

    authentication_event = "failed"

AND

    failed_attempts >= defined_threshold

WITHIN

    defined_time_window

THEN

    generate_security_alert
```

## Example Detection Scenario

A security monitoring platform observes multiple failed authentication attempts against an account within a short period.

The system generates:

```text id="r5c1qa"
Alert: Repeated Authentication Failures

Severity: Medium
Category: Authentication
Action: Investigate
```

## Relevant Fields

A SOC analyst should review available fields such as:

| Field                 | Purpose                     |
| --------------------- | --------------------------- |
| Username              | Identify targeted account   |
| Source IP             | Identify connection origin  |
| Timestamp             | Establish activity timeline |
| Hostname              | Identify affected system    |
| Authentication method | Understand login mechanism  |
| Result                | Determine success/failure   |
| Failure reason        | Identify possible cause     |

## Investigation Questions

When the alert triggers, the analyst should ask:

1. Is the activity expected?
2. Is one account or multiple accounts being targeted?
3. Is the source known?
4. Was a successful login observed afterward?
5. Is the targeted account privileged?
6. Are there related alerts?
7. Does the activity match normal user behavior?

## False Positive Considerations

Potential legitimate causes include:

* User forgetting a password
* Incorrect stored credentials
* Application configuration problems
* Expired credentials
* Automated services using outdated credentials

Detection thresholds should therefore be tuned to the organization's normal behavior.

## Escalation Conditions

Consider increasing severity when evidence indicates:

* Multiple accounts targeted
* Successful authentication after repeated failures
* Privileged account targeted
* Suspicious source infrastructure
* Unusual geographic origin
* Additional suspicious activity

## MITRE ATT&CK

Potential mapping:

**T1110 — Brute Force**

Additional sub-technique classification should depend on the observed evidence.

## Recommended Response

If malicious activity is confirmed:

* Preserve relevant logs
* Investigate the source
* Validate the affected account
* Review successful authentication
* Apply appropriate account protections
* Investigate related activity
* Document the incident

## Detection Lifecycle

```text id="3p7xvf"
Create Rule
    ↓
Test
    ↓
Tune Thresholds
    ↓
Monitor Alerts
    ↓
Investigate
    ↓
Reduce False Positives
    ↓
Review & Improve
```

## Status

**Detection Design Complete**

This rule is a documented detection concept and does not claim deployment to a production SIEM.
