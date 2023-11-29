Rules by Product and UseCase
============================
Vendor: Quest Software
----------------------
### Product: [Quest Change Auditor for Active Directory](../ds_quest_software_quest_change_auditor_for_active_directory.md)
### Use-Case: [Privilege Escalation](../../../../UseCases/uc_privilege_escalation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   1    |         2          |       2        |    2    |

| Event Type   | Rules    | Models    |
| ---- | ---- | ---- |
| local-logon  | <b>T1078 - Valid Accounts</b><br> ↳ <b>AS-PV-UHWoPC</b>: Access to Password Vault managed asset with no password checkout for user<br><br><b>T1555.005 - T1555.005</b><br> ↳ <b>AS-PV-UHWoPC</b>: Access to Password Vault managed asset with no password checkout for user |  • <b>AS-PV-OA</b>: Password retrieval based accounts |
| remote-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>AS-PV-UHWoPC</b>: Access to Password Vault managed asset with no password checkout for user<br><br><b>T1555.005 - T1555.005</b><br> ↳ <b>AS-PV-UHWoPC</b>: Access to Password Vault managed asset with no password checkout for user |  • <b>AS-PV-OA</b>: Password retrieval based accounts |