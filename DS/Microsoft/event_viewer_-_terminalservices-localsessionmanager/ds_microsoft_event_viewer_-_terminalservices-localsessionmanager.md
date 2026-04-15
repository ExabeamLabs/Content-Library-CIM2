Vendor: Microsoft
=================
Product: Event Viewer - TerminalServices-LocalSessionManager
------------------------------------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   0    |         1          |       1        |    0    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Lateral Movement](../../../UseCases/uc_lateral_movement.md) |  logout-remote<br> ↳[microsoft-windows-kv-endpoint-logout-success-23](Ps/pC_microsoftwindowskvendpointlogoutsuccess23.md)<br> | T1210 - Exploitation of Remote Services<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_event_viewer_-_terminalservices-localsessionmanager_Lateral_Movement.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement                                                                     | Collection | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ------------------------------------------------------------------------------------ | ---------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           | [Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210)<br><br> |            |                     |              |        |