Rules by Product and UseCase
============================
Vendor: BeyondTrust
-------------------
### Product: [BeyondTrust Remote Support](../ds_beyondtrust_beyondtrust_remote_support.md)
### Use-Case: [Workforce Protection](../../../../UseCases/uc_workforce_protection.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   1    |         2          |       2        |    1    |

| Event Type          | Rules    | Models    |
| ---- | ---- | ---- |
| web-meeting-started | <b>T1078 - Valid Accounts</b><br> ↳ <b>WCA-MTOW-A</b>: Abnormal web conference meeting time<br><br><b>T1078.004 - Valid Accounts: Cloud Accounts</b><br> ↳ <b>WCA-MTOW-A</b>: Abnormal web conference meeting time |  • <b>WCA-MTOW</b>: Web conference meeting start time for user |
| web-meeting-updated | <b>T1078 - Valid Accounts</b><br> ↳ <b>WCA-DP</b>: Meeting updated to remove password<br><br><b>T1078.004 - Valid Accounts: Cloud Accounts</b><br> ↳ <b>WCA-DP</b>: Meeting updated to remove password    |    |