Vendor: Microsoft
=================
Product: Event Viewer - DHCP-Server
-----------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         2          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
|    [Lateral Movement](../../../UseCases/uc_lateral_movement.md)    |  app-activity-failed<br> ↳[microsoft-evdhcpserver-sk4-app-activity-fail-adminevents](Ps/pC_microsoftevdhcpserversk4appactivityfailadminevents.md)<br> | T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_event_viewer_-_dhcp-server_Lateral_Movement.md)    |
|     [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)     |  app-activity-failed<br> ↳[microsoft-evdhcpserver-sk4-app-activity-fail-adminevents](Ps/pC_microsoftevdhcpserversk4appactivityfailadminevents.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_event_viewer_-_dhcp-server_Privilege_Abuse.md)     |
| [Privileged Activity](../../../UseCases/uc_privileged_activity.md) |  app-activity-failed<br> ↳[microsoft-evdhcpserver-sk4-app-activity-fail-adminevents](Ps/pC_microsoftevdhcpserversk4appactivityfailadminevents.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_event_viewer_-_dhcp-server_Privileged_Activity.md) |
|          [Ransomware](../../../UseCases/uc_ransomware.md)          |  app-activity-failed<br> ↳[microsoft-evdhcpserver-sk4-app-activity-fail-adminevents](Ps/pC_microsoftevdhcpserversk4appactivityfailadminevents.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_event_viewer_-_dhcp-server_Ransomware.md)          |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |