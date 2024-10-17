Vendor: Unix
============
Product: Unix Privilege Management
----------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  16   |   9    |         4          |       1        |    0    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  user-switch:success (account-switch)<br> ↳[unix-privmgmt-str-user-switch-success-acceptedsu](Ps/pC_unixprivmgmtstruserswitchsuccessacceptedsu.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_unix_unix_privilege_management_Abnormal_Authentication_&_Access.md) |
|    [Malware](../../../UseCases/uc_malware.md)    |  user-switch:success (account-switch)<br> ↳[unix-privmgmt-str-user-switch-success-acceptedsu](Ps/pC_unixprivmgmtstruserswitchsuccessacceptedsu.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_unix_unix_privilege_management_Malware.md)    |
|    [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)    |  user-switch:success (account-switch)<br> ↳[unix-privmgmt-str-user-switch-success-acceptedsu](Ps/pC_unixprivmgmtstruserswitchsuccessacceptedsu.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_unix_unix_privilege_management_Privilege_Abuse.md)    |
|    [Privilege Escalation](../../../UseCases/uc_privilege_escalation.md)    |  user-switch:success (account-switch)<br> ↳[unix-privmgmt-str-user-switch-success-acceptedsu](Ps/pC_unixprivmgmtstruserswitchsuccessacceptedsu.md)<br> | T1078 - Valid Accounts<br>T1555 - Credentials from Password Stores<br>T1555.005 - T1555.005<br> | [<ul><li>10 Rules</li></ul><ul><li>7 Models</li></ul>](RM/r_m_unix_unix_privilege_management_Privilege_Escalation.md)    |
|    [Privileged Activity](../../../UseCases/uc_privileged_activity.md)    |  user-switch:success (account-switch)<br> ↳[unix-privmgmt-str-user-switch-success-acceptedsu](Ps/pC_unixprivmgmtstruserswitchsuccessacceptedsu.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_unix_unix_privilege_management_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access                                                                     | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Credentials from Password Stores](https://attack.mitre.org/techniques/T1555)<br><br> |           |                  |            |                     |              |        |