Vendor: Microsoft
=================
Product: Event Viewer - DNSServer
---------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   0    |     2      |       4        |    4    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Malware](../../../UseCases/uc_malware.md) |  ""app-notification:success""<br> ↳[microsoft-evdnsserver-xml-app-notification-3150](Ps/pC_microsoftevdnsserverxmlappnotification3150.md)<br><br> ""dns-traffic:fail""<br> ↳[microsoft-evdnsserver-xml-dns-traffic-fail-5502](Ps/pC_microsoftevdnsserverxmldnstrafficfail5502.md)<br><br> ""network-notification:success""<br> ↳[microsoft-evdnsserver-xml-network-notification-6522](Ps/pC_microsoftevdnsserverxmlnetworknotification6522.md)<br> ↳[microsoft-evdnsserver-xml-network-notification-6004](Ps/pC_microsoftevdnsserverxmlnetworknotification6004.md)<br> ↳[microsoft-evdnsserver-xml-network-notification-6001](Ps/pC_microsoftevdnsserverxmlnetworknotification6001.md)<br><br> dns-response<br> ↳[microsoft-evdnsserver-xml-dns-response-fail-7050](Ps/pC_microsoftevdnsserverxmldnsresponsefail7050.md)<br> | T1071 - Application Layer Protocol<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br> | [<ul><li>2 Rules</li></ul>](RM/r_m_microsoft_event_viewer_-_dnsserver_Malware.md) |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                                                             | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Dynamic Resolution](https://attack.mitre.org/techniques/T1568)<br><br>[Dynamic Resolution: Domain Generation Algorithms](https://attack.mitre.org/techniques/T1568/002)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> |              |        |