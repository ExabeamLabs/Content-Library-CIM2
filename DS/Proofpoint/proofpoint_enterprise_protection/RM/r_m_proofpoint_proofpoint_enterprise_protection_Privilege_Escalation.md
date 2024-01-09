Rules by Product and UseCase
============================
Vendor: Proofpoint
------------------
### Product: [Proofpoint Enterprise Protection](../ds_proofpoint_proofpoint_enterprise_protection.md)
### Use-Case: [Privilege Escalation](../../../../UseCases/uc_privilege_escalation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   1    |         2          |       1        |    0    |

| Event Type   | Rules    | Models    |
| ---- | ---- | ---- |
| remote-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>AS-PV-UHWoPC</b>: Access to Password Vault managed asset with no password checkout for user<br> ↳ <b>DC18-new</b>: Account switch by new user<br><br><b>T1555.005 - T1555.005</b><br> ↳ <b>AS-PV-UHWoPC</b>: Access to Password Vault managed asset with no password checkout for user |  • <b>AS-PV-OA</b>: Password retrieval based accounts |