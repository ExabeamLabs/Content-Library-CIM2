Rules by Product and UseCase
============================
Vendor: CA Technologies
-----------------------
### Product: [CA Privileged Access Manager Server Control](../ds_ca_technologies_ca_privileged_access_manager_server_control.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   0    |         1          |       2        |    2    |

| Event Type     | Rules    | Models |
| ---- | ---- | ------ |
| account-switch | <b>T1078 - Valid Accounts</b><br> ↳ <b>AS-UA-F-PRIV</b>: Account switch to a privileged or executive account<br> ↳ <b>DC18-New</b>: New account switch to privileged account      |        |
| app-login      | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-F-SA-NC</b>: New service account access to application |        |