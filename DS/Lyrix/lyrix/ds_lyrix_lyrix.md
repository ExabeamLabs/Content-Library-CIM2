Vendor: Lyrix
=============
Product: Lyrix
--------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  12   |   6    |         1          |       1        |    1    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP          | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  physical_location-access:fail (failed-physical-access)<br> ↳[lyrix-l-cef-physical-location-access-success-doorname](Ps/pC_lyrixlcefphysicallocationaccesssuccessdoorname.md)<br> ↳[lyrix-l-cef-physical-location-access-success-department](Ps/pC_lyrixlcefphysicallocationaccesssuccessdepartment.md)<br><br> physical_location-access:success (physical-access)<br> ↳[lyrix-l-cef-physical-location-access-success-doorname](Ps/pC_lyrixlcefphysicallocationaccesssuccessdoorname.md)<br> ↳[lyrix-l-cef-physical-location-access-success-department](Ps/pC_lyrixlcefphysicallocationaccesssuccessdepartment.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>3 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_lyrix_lyrix_Abnormal_Authentication_&_Access.md) |
|    [Physical Security](../../../UseCases/uc_physical_security.md)    |  physical_location-access:fail (failed-physical-access)<br> ↳[lyrix-l-cef-physical-location-access-success-doorname](Ps/pC_lyrixlcefphysicallocationaccesssuccessdoorname.md)<br> ↳[lyrix-l-cef-physical-location-access-success-department](Ps/pC_lyrixlcefphysicallocationaccesssuccessdepartment.md)<br><br> physical_location-access:success (physical-access)<br> ↳[lyrix-l-cef-physical-location-access-success-doorname](Ps/pC_lyrixlcefphysicallocationaccesssuccessdoorname.md)<br> ↳[lyrix-l-cef-physical-location-access-success-department](Ps/pC_lyrixlcefphysicallocationaccesssuccessdepartment.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>9 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_lyrix_lyrix_Physical_Security.md)    |
[Next Page -->>](2_ds_lyrix_lyrix.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |