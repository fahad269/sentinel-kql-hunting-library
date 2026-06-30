# MITRE ATT&CK Coverage Matrix

Rows are filled in as each query is built. Identity domain is complete.

| Technique ID | Technique Name | Query File | Domain |
|---|---|---|---|
| T1078.004 | Valid Accounts: Cloud Accounts | identity/impossible-travel-signin.kql | Identity |
| T1621 | Multi-Factor Authentication Request Generation | identity/mfa-fatigue-pattern.kql | Identity |
| T1550.001 | Use Alternate Authentication Material: Application Access Token | identity/suspicious-oauth-consent.kql | Identity |
| T1528 | Steal Application Access Token | identity/suspicious-oauth-consent.kql | Identity |
| T1098 | Account Manipulation | identity/privilege-escalation-role-changes.kql | Identity |
| T1078.004 | Valid Accounts: Cloud Accounts | identity/stale-privileged-account.kql | Identity |
| T1556.006 | Modify Authentication Process: Multi-Factor Authentication | identity/conditional-access-bypass.kql | Identity |
| T1218 | System Binary Proxy Execution | endpoint/lolbin-execution.kql | Endpoint |
| T1055 | Process Injection | endpoint/suspicious-process-tree.kql | Endpoint |
| T1199 | Trusted Relationship | endpoint/unmanaged-device-access.kql | Endpoint |
| T1003 | OS Credential Dumping | endpoint/credential-dumping-indicators.kql | Endpoint |
| T1053 | Scheduled Task/Job | endpoint/persistence-scheduled-task.kql | Endpoint |
| T1562.001 | Impair Defenses: Disable or Modify Tools | endpoint/defender-tampering.kql | Endpoint |

> Remaining domains (network, cloud, data-exfiltration, insider-threat) will be
> added as those queries are built.

## Note on the two corrected mappings

Two techniques in the original project blueprint were refined during the
Identity build:

- **MFA fatigue / push-bombing** maps to **T1621 (Multi-Factor Authentication
  Request Generation)**, the technique created specifically for prompt-bombing,
  rather than the broader T1556.
- **OAuth consent abuse** is cross-mapped to **T1528 (Steal Application Access
  Token)** alongside T1550.001, since the consent grant itself is the
  token-theft primitive.
