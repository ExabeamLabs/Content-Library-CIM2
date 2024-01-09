Vendor: RS2 Technologies
========================
Product: RS2 Technologies
-------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  12   |   6    |         1          |       1        |    0    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP          | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  failed-physical-access<br> ↳[rs2-t-xml-physical-location-access-fail-elevatoraccessdenied](Ps/pC_rs2txmlphysicallocationaccessfailelevatoraccessdenied.md)<br><br> physical-access<br> ↳[rs2-t-xml-physical-location-access-success-elevatoraccessgranted](Ps/pC_rs2txmlphysicallocationaccesssuccesselevatoraccessgranted.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>3 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_rs2_technologies_rs2_technologies_Abnormal_Authentication_&_Access.md) |
|    [Physical Security](../../../UseCases/uc_physical_security.md)    |  failed-physical-access<br> ↳[rs2-t-xml-physical-location-access-fail-elevatoraccessdenied](Ps/pC_rs2txmlphysicallocationaccessfailelevatoraccessdenied.md)<br><br> physical-access<br> ↳[rs2-t-xml-physical-location-access-success-elevatoraccessgranted](Ps/pC_rs2txmlphysicallocationaccesssuccesselevatoraccessgranted.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>9 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_rs2_technologies_rs2_technologies_Physical_Security.md)    |
|    [Privileged Activity](../../../UseCases/uc_privileged_activity.md)    |  failed-physical-access<br> ↳[rs2-t-xml-physical-location-access-fail-elevatoraccessdenied](Ps/pC_rs2txmlphysicallocationaccessfailelevatoraccessdenied.md)<br><br> physical-access<br> ↳[rs2-t-xml-physical-location-access-success-elevatoraccessgranted](Ps/pC_rs2txmlphysicallocationaccesssuccesselevatoraccessgranted.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_rs2_technologies_rs2_technologies_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |