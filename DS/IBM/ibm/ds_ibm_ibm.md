Vendor: IBM
===========
Product: IBM
------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  58   |   26   |         8          |       2        |    0    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  scheduled_task-trigger:success (app-activity)<br> ↳[ibm-i-str-app-activity-success-binddn](Ps/pC_ibmistrappactivitysuccessbinddn.md)<br><br> endpoint-login:success (authentication-successful)<br> ↳[ibm-i-str-app-authentication-success-indbinddn](Ps/pC_ibmistrappauthenticationsuccessindbinddn.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>12 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_ibm_ibm_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[ibm-i-str-app-activity-success-binddn](Ps/pC_ibmistrappactivitysuccessbinddn.md)<br>    | T1098 - Account Manipulation<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>    | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_ibm_ibm_Account_Manipulation.md)    |
|          [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md)          |  scheduled_task-trigger:success (app-activity)<br> ↳[ibm-i-str-app-activity-success-binddn](Ps/pC_ibmistrappactivitysuccessbinddn.md)<br><br> endpoint-login:success (authentication-successful)<br> ↳[ibm-i-str-app-authentication-success-indbinddn](Ps/pC_ibmistrappauthenticationsuccessindbinddn.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>39 Rules</li></ul><ul><li>24 Models</li></ul>](RM/r_m_ibm_ibm_Compromised_Credentials.md)         |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[ibm-i-str-app-activity-success-binddn](Ps/pC_ibmistrappactivitysuccessbinddn.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>19 Rules</li></ul><ul><li>11 Models</li></ul>](RM/r_m_ibm_ibm_Data_Access.md)    |
|    [Data Leak](../../../UseCases/uc_data_leak.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[ibm-i-str-app-activity-success-binddn](Ps/pC_ibmistrappactivitysuccessbinddn.md)<br>    | T1114 - Email Collection<br>T1114.003 - Email Collection: Email Forwarding Rule<br>    | [<ul><li>3 Rules</li></ul>](RM/r_m_ibm_ibm_Data_Leak.md)    |
|    [Lateral Movement](../../../UseCases/uc_lateral_movement.md)    |  endpoint-login:success (authentication-successful)<br> ↳[ibm-i-str-app-authentication-success-indbinddn](Ps/pC_ibmistrappauthenticationsuccessindbinddn.md)<br>    | T1090 - Proxy<br>T1090.003 - Proxy: Multi-hop Proxy<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_ibm_ibm_Lateral_Movement.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  endpoint-login:success (authentication-successful)<br> ↳[ibm-i-str-app-authentication-success-indbinddn](Ps/pC_ibmistrappauthenticationsuccessindbinddn.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_ibm_ibm_Malware.md)    |
|    [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[ibm-i-str-app-activity-success-binddn](Ps/pC_ibmistrappactivitysuccessbinddn.md)<br>    | T1078 - Valid Accounts<br>T1098 - Account Manipulation<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br> | [<ul><li>6 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_ibm_ibm_Privilege_Abuse.md)    |
|    [Privilege Escalation](../../../UseCases/uc_privilege_escalation.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[ibm-i-str-app-activity-success-binddn](Ps/pC_ibmistrappactivitysuccessbinddn.md)<br>    | T1098 - Account Manipulation<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>    | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_ibm_ibm_Privilege_Escalation.md)    |
|    [Privileged Activity](../../../UseCases/uc_privileged_activity.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[ibm-i-str-app-activity-success-binddn](Ps/pC_ibmistrappactivitysuccessbinddn.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_ibm_ibm_Privileged_Activity.md)    |
|    [Ransomware](../../../UseCases/uc_ransomware.md)    |  endpoint-login:success (authentication-successful)<br> ↳[ibm-i-str-app-authentication-success-indbinddn](Ps/pC_ibmistrappauthenticationsuccessindbinddn.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_ibm_ibm_Ransomware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                                                                                   | Execution | Persistence                                                                                                                                                                                                                                                                                                                                 | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection                                                                                                                                                            | Command and Control                                                                                                                       | Exfiltration | Impact |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  | [Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |