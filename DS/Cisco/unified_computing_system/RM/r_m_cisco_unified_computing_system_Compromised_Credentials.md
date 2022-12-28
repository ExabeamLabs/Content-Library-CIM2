Rules by Product and UseCase
============================
Vendor: Cisco
-------------
### Product: [Unified Computing System](../ds_cisco_unified_computing_system.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   3   |   1    |     1      |       1        |    1    |

| Event Type   | Rules    | Models    |
| ---- | ---- | ---- |
| failed-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-04</b>: Failed logon by a service account<br> ↳ <b>SEQ-UH-05</b>: Failed interactive logon by a service account<br> ↳ <b>SEQ-UH-07</b>: Failed logon to an asset that user has not previously accessed |  • <b>AE-UA</b>: All activity for users |