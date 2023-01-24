Rules by Product and UseCase
============================
Vendor: APC
-----------
### Product: [APC](../ds_apc_apc.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   1    |         1          |       5        |    5    |

| Event Type       | Rules    | Models    |
| ---- | ---- | ---- |
| failed-app-login | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-F-FL</b>: Failed login to application    |    |
| failed-logon     | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-04</b>: Failed logon by a service account<br> ↳ <b>SEQ-UH-05</b>: Failed interactive logon by a service account<br> ↳ <b>SEQ-UH-07</b>: Failed logon to an asset that user has not previously accessed |  • <b>AE-UA</b>: All activity for users |