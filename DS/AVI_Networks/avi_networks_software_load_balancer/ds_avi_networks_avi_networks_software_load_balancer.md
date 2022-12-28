Vendor: AVI Networks
====================
Product: AVI Networks Software Load Balancer
--------------------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   1   |   0    |     1      |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Lateral Movement](../../../UseCases/uc_lateral_movement.md) |  logout-remote<br> ↳[avinetworks-lb-str-endpoint-logout-userlogout](Ps/pC_avinetworkslbstrendpointlogoutuserlogout.md)<br> | T1210 - Exploitation of Remote Services<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_avi_networks_avi_networks_software_load_balancer_Lateral_Movement.md) |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement                                                                     | Collection | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ------------------------------------------------------------------------------------ | ---------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           | [Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210)<br><br> |            |                     |              |        |