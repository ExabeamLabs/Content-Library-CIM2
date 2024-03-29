Vendor: Dell
============
Product: One Identity Manager
-----------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  16   |   9    |         3          |       1        |    0    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  account-switch<br> ↳[dell-oim-cef-user-switch-success-retrievepassword](Ps/pC_delloimcefuserswitchsuccessretrievepassword.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_dell_one_identity_manager_Abnormal_Authentication_&_Access.md) |
|    [Malware](../../../UseCases/uc_malware.md)    |  account-switch<br> ↳[dell-oim-cef-user-switch-success-retrievepassword](Ps/pC_delloimcefuserswitchsuccessretrievepassword.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_dell_one_identity_manager_Malware.md)    |
|    [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)    |  account-switch<br> ↳[dell-oim-cef-user-switch-success-retrievepassword](Ps/pC_delloimcefuserswitchsuccessretrievepassword.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_dell_one_identity_manager_Privilege_Abuse.md)    |
|    [Privilege Escalation](../../../UseCases/uc_privilege_escalation.md)    |  account-switch<br> ↳[dell-oim-cef-user-switch-success-retrievepassword](Ps/pC_delloimcefuserswitchsuccessretrievepassword.md)<br> | T1078 - Valid Accounts<br>T1555.005 - T1555.005<br> | [<ul><li>10 Rules</li></ul><ul><li>6 Models</li></ul>](RM/r_m_dell_one_identity_manager_Privilege_Escalation.md)    |
|    [Privileged Activity](../../../UseCases/uc_privileged_activity.md)    |  account-switch<br> ↳[dell-oim-cef-user-switch-success-retrievepassword](Ps/pC_delloimcefuserswitchsuccessretrievepassword.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_dell_one_identity_manager_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access                                                                     | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Credentials from Password Stores](https://attack.mitre.org/techniques/T1555)<br><br> |           |                  |            |                     |              |        |