Vendor: Microsoft
=================
Product: Microsoft DNS Log
--------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   0    |         3          |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Malware](../../../UseCases/uc_malware.md) |  dns-query<br> ↳[microsoft-windows-str-dns-request-success-queryq](Ps/pC_microsoftwindowsstrdnsrequestsuccessqueryq.md)<br> ↳[microsoft-windows-str-dns-request-success-packetu](Ps/pC_microsoftwindowsstrdnsrequestsuccesspacketu.md)<br> ↳[microsoft-windows-str-dns-request-success-packetn](Ps/pC_microsoftwindowsstrdnsrequestsuccesspacketn.md)<br><br> dns-response<br> ↳[microsoft-windows-str-dns-response-success-packetru](Ps/pC_microsoftwindowsstrdnsresponsesuccesspacketru.md)<br> ↳[microsoft-windows-str-dns-response-success-packetrq](Ps/pC_microsoftwindowsstrdnsresponsesuccesspacketrq.md)<br> ↳[microsoft-windows-kv-dns-response-success-udpresponseinfo](Ps/pC_microsoftwindowskvdnsresponsesuccessudpresponseinfo.md)<br> | T1071 - Application Layer Protocol<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br>T1583.001 - T1583.001<br> | [<ul><li>5 Rules</li></ul>](RM/r_m_microsoft_microsoft_dns_log_Malware.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                                                             | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Dynamic Resolution](https://attack.mitre.org/techniques/T1568)<br><br>[Dynamic Resolution: Domain Generation Algorithms](https://attack.mitre.org/techniques/T1568/002)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> |              |        |