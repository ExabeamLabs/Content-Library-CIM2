Rules by Product and UseCase
============================
Vendor: HP
----------
### Product: [ArubaOS](../ds_hp_arubaos.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   3    |         2          |       1        |    3    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| nac-logon  | <b>T1021 - Remote Services</b><br> ↳ <b>NAC-OAt-F</b>: First authentication type for organization<br> ↳ <b>NAC-OAt-A</b>: Abnormal authentication type for organization<br> ↳ <b>NAC-GAt-F</b>: First authentication type for peer group<br> ↳ <b>NAC-GAt-A</b>: Abnormal authentication type for peer group<br> ↳ <b>NAC-UAt-F</b>: First authentication type for user<br> ↳ <b>NAC-UAt-A</b>: Abnormal authentication type for user<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>NAC-UAt-F</b>: First authentication type for user<br> ↳ <b>NAC-UAt-A</b>: Abnormal authentication type for user |  • <b>NAC-UAt</b>: Authentication Types for user<br> • <b>NAC-GAt</b>: Authentication Types for peer group<br> • <b>NAC-OAt</b>: Authentication Types for organization |