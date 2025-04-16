Vendor: BlueCat Networks
========================
Product: BlueCat Networks
-------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   0    |         5          |       2        |    3    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Malware](../../../UseCases/uc_malware.md) |  dns-request:success (dns-query)<br> ↳[bluecatnetworks-bnetworks-leef-dns-request-success-bcn](Ps/pC_bluecatnetworksbnetworksleefdnsrequestsuccessbcn.md)<br> ↳[bluecatnetworks-bnetworks-json-dns-request-query](Ps/pC_bluecatnetworksbnetworksjsondnsrequestquery.md)<br> ↳[bluecatnetworks-bnetworks-json-dns-request-query](Ps/pC_bluecatnetworksbnetworksjsondnsrequestquery.md)<br><br> dns-response:success (dns-response)<br> ↳[bluecatnetworks-bnetworks-json-dns-response-queryresponse](Ps/pC_bluecatnetworksbnetworksjsondnsresponsequeryresponse.md)<br> ↳[bluecatnetworks-bnetworks-json-dns-response-queryresponse](Ps/pC_bluecatnetworksbnetworksjsondnsresponsequeryresponse.md)<br> | T1071 - Application Layer Protocol<br>T1568 - Dynamic Resolution<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br>T1583 - T1583<br>T1583.001 - T1583.001<br> | [<ul><li>5 Rules</li></ul>](RM/r_m_bluecat_networks_bluecat_networks_Malware.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                                                             | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Dynamic Resolution](https://attack.mitre.org/techniques/T1568)<br><br>[Dynamic Resolution: Domain Generation Algorithms](https://attack.mitre.org/techniques/T1568/002)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> |              |        |