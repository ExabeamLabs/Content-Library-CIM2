Vendor: ICPAM
=============
Product: ICPAM
--------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  10   |   5    |         1          |       1        |    0    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP          | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  physical_location-access:success (physical-access)<br> ↳[icpam-i-kv-physical-location-access-success-granted](Ps/pC_icpamikvphysicallocationaccesssuccessgranted.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>3 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_icpam_icpam_Abnormal_Authentication_&_Access.md) |
|    [Physical Security](../../../UseCases/uc_physical_security.md)    |  physical_location-access:success (physical-access)<br> ↳[icpam-i-kv-physical-location-access-success-granted](Ps/pC_icpamikvphysicallocationaccesssuccessgranted.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>7 Rules</li></ul><ul><li>3 Models</li></ul>](RM/r_m_icpam_icpam_Physical_Security.md)    |
|    [Privileged Activity](../../../UseCases/uc_privileged_activity.md)    |  physical_location-access:success (physical-access)<br> ↳[icpam-i-kv-physical-location-access-success-granted](Ps/pC_icpamikvphysicallocationaccesssuccessgranted.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_icpam_icpam_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |