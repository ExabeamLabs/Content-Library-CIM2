Vendor: DXC
===========
Product: DXC Technology
-----------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   3    |         3          |       1        |    0    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  authentication-failed<br> ↳[dxc-dxctech-str-app-notification-dxcnetwork](Ps/pC_dxcdxctechstrappnotificationdxcnetwork.md)<br> | T1133 - External Remote Services<br>    | [<ul><li>3 Rules</li></ul><ul><li>3 Models</li></ul>](RM/r_m_dxc_dxc_technology_Abnormal_Authentication_&_Access.md) |
|    [Lateral Movement](../../../UseCases/uc_lateral_movement.md)    |  authentication-failed<br> ↳[dxc-dxctech-str-app-notification-dxcnetwork](Ps/pC_dxcdxctechstrappnotificationdxcnetwork.md)<br> | T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_dxc_dxc_technology_Lateral_Movement.md)    |
|    [Ransomware](../../../UseCases/uc_ransomware.md)    |  authentication-failed<br> ↳[dxc-dxctech-str-app-notification-dxcnetwork](Ps/pC_dxcdxctechstrappnotificationdxcnetwork.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_dxc_dxc_technology_Ransomware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                                                                                   | Execution | Persistence                                                                                                                                      | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |