Vendor: Microsoft
=================
Product: Event Viewer - DHCP-Server
-----------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         1          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP       | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  account-lockout<br> ↳[microsoft-evdhcpserver-sk4-app-activity-fail-adminevents](Ps/pC_microsoftevdhcpserversk4appactivityfailadminevents.md)<br> ↳[microsoft-evdhcpserver-sk4-dns-record-create-fail-adminevents](Ps/pC_microsoftevdhcpserversk4dnsrecordcreatefailadminevents.md)<br> | T1110 - Brute Force<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_event_viewer_-_dhcp-server_Abnormal_Authentication_&_Access.md) |
|    [Brute Force Attack](../../../UseCases/uc_brute_force_attack.md)    |  account-lockout<br> ↳[microsoft-evdhcpserver-sk4-app-activity-fail-adminevents](Ps/pC_microsoftevdhcpserversk4appactivityfailadminevents.md)<br> ↳[microsoft-evdhcpserver-sk4-dns-record-create-fail-adminevents](Ps/pC_microsoftevdhcpserversk4dnsrecordcreatefailadminevents.md)<br> | T1110 - Brute Force<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_event_viewer_-_dhcp-server_Brute_Force_Attack.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access                                                | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ---------------------------------------------------------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 | [Brute Force](https://attack.mitre.org/techniques/T1110)<br><br> |           |                  |            |                     |              |        |