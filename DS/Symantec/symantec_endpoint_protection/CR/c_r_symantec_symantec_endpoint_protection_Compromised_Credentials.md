Correlation Rules by Product and UseCase
========================================
Vendor: Symantec
----------------
### Product: [Symantec Endpoint Protection](../ds_symantec_symantec_endpoint_protection.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Name    | Description    | Activity Type | MITRE Tactic      | Severity | Overlap with AA |
| ---- | ---- | ---- | ---- | -------- | ---- |
| Passwd or Shadow file read.    | Passwd or Shadow file was read. This file stores essential information about the users on the system. | file-read     | Credential Access | 2        | false    |
| UBA: Multiple VPN logins from single IP. | Multiple VPN login attempts were detected from a single IP address within a specific time frame.      | vpn-login     | Credential Access | 2        | false    |