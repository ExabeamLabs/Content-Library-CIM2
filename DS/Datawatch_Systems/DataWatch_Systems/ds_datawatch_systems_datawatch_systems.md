Vendor: Datawatch Systems
=========================
Product: DataWatch Systems
--------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  12   |   6    |     1      |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  failed-physical-access<br> ↳[datawatch-ds-str-physical_location-access-badgeaccess](Ps/pC_datawatchdsstrphysical_locationaccessbadgeaccess.md)<br><br> physical-access<br> ↳[datawatch-ds-str-physical_location-access-badgeaccess](Ps/pC_datawatchdsstrphysical_locationaccessbadgeaccess.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>3 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_datawatch_systems_datawatch_systems_Abnormal_Authentication_&_Access.md) |
|    [Physical Security](../../../UseCases/uc_physical_security.md)    |  failed-physical-access<br> ↳[datawatch-ds-str-physical_location-access-badgeaccess](Ps/pC_datawatchdsstrphysical_locationaccessbadgeaccess.md)<br><br> physical-access<br> ↳[datawatch-ds-str-physical_location-access-badgeaccess](Ps/pC_datawatchdsstrphysical_locationaccessbadgeaccess.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>9 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_datawatch_systems_datawatch_systems_Physical_Security.md)    |
|    [Privileged Activity](../../../UseCases/uc_privileged_activity.md)    |  failed-physical-access<br> ↳[datawatch-ds-str-physical_location-access-badgeaccess](Ps/pC_datawatchdsstrphysical_locationaccessbadgeaccess.md)<br><br> physical-access<br> ↳[datawatch-ds-str-physical_location-access-badgeaccess](Ps/pC_datawatchdsstrphysical_locationaccessbadgeaccess.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_datawatch_systems_datawatch_systems_Privileged_Activity.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |