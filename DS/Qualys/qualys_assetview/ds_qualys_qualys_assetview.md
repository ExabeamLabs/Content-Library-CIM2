Vendor: Qualys
==============
Product: Qualys AssetView
-------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  85   |   37   |         11         |       2        |    0    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  scheduled_task-trigger:success (app-activity)<br> ↳[qualys-q-json-app-activity-success-scan](Ps/pC_qualysqjsonappactivitysuccessscan.md)<br>    | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>12 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_qualys_qualys_assetview_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[qualys-q-json-app-activity-success-scan](Ps/pC_qualysqjsonappactivitysuccessscan.md)<br>    | T1098 - Account Manipulation<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>    | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_qualys_qualys_assetview_Account_Manipulation.md)    |
|          [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md)          |  scheduled_task-trigger:success (app-activity)<br> ↳[qualys-q-json-app-activity-success-scan](Ps/pC_qualysqjsonappactivitysuccessscan.md)<br><br> alert-trigger:success (security-alert)<br> ↳[qualys-q-kv-alert-trigger-success-scan](Ps/pC_qualysqkvalerttriggersuccessscan.md)<br> | T1027 - Obfuscated Files or Information<br>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>T1078 - Valid Accounts<br>T1133 - External Remote Services<br>T1190 - Exploit Public Fasing Application<br> | [<ul><li>62 Rules</li></ul><ul><li>33 Models</li></ul>](RM/r_m_qualys_qualys_assetview_Compromised_Credentials.md)         |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[qualys-q-json-app-activity-success-scan](Ps/pC_qualysqjsonappactivitysuccessscan.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>19 Rules</li></ul><ul><li>11 Models</li></ul>](RM/r_m_qualys_qualys_assetview_Data_Access.md)    |
|    [Data Leak](../../../UseCases/uc_data_leak.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[qualys-q-json-app-activity-success-scan](Ps/pC_qualysqjsonappactivitysuccessscan.md)<br>    | T1114 - Email Collection<br>T1114.003 - Email Collection: Email Forwarding Rule<br>    | [<ul><li>3 Rules</li></ul>](RM/r_m_qualys_qualys_assetview_Data_Leak.md)    |
|    [Lateral Movement](../../../UseCases/uc_lateral_movement.md)    |  alert-trigger:success (security-alert)<br> ↳[qualys-q-kv-alert-trigger-success-scan](Ps/pC_qualysqkvalerttriggersuccessscan.md)<br>    | T1027 - Obfuscated Files or Information<br>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_qualys_qualys_assetview_Lateral_Movement.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  alert-trigger:success (security-alert)<br> ↳[qualys-q-kv-alert-trigger-success-scan](Ps/pC_qualysqkvalerttriggersuccessscan.md)<br>    | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_qualys_qualys_assetview_Malware.md)    |
|    [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[qualys-q-json-app-activity-success-scan](Ps/pC_qualysqjsonappactivitysuccessscan.md)<br>    | T1078 - Valid Accounts<br>T1098 - Account Manipulation<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>    | [<ul><li>6 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_qualys_qualys_assetview_Privilege_Abuse.md)    |
|    [Privilege Escalation](../../../UseCases/uc_privilege_escalation.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[qualys-q-json-app-activity-success-scan](Ps/pC_qualysqjsonappactivitysuccessscan.md)<br>    | T1098 - Account Manipulation<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>    | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_qualys_qualys_assetview_Privilege_Escalation.md)    |
|    [Privileged Activity](../../../UseCases/uc_privileged_activity.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[qualys-q-json-app-activity-success-scan](Ps/pC_qualysqjsonappactivitysuccessscan.md)<br><br> alert-trigger:success (security-alert)<br> ↳[qualys-q-kv-alert-trigger-success-scan](Ps/pC_qualysqkvalerttriggersuccessscan.md)<br> | T1068 - Exploitation for Privilege Escalation<br>T1078 - Valid Accounts<br>    | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_qualys_qualys_assetview_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                                                                                                                                                                                                                 | Privilege Escalation                                                                                                                                          | Defense Evasion                                                                                                                                                                                                                                                               | Credential Access | Discovery | Lateral Movement | Collection                                                                                                                                                            | Command and Control | Exfiltration | Impact |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068)<br><br> | [Obfuscated Files or Information: Indicator Removal from Tools](https://attack.mitre.org/techniques/T1027/005)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027)<br><br> |                   |           |                  | [Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> |                     |              |        |