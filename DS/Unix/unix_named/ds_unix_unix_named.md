Vendor: Unix
============
Product: Unix Named
-------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         5          |       1        |    2    |

|    Use-Case    | Activity Types(Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Malware](../../../UseCases/uc_malware.md) |  dns-request:success(dns-query)<br> ↳[unix-unixnamed-str-dns-request-success-client](Ps/pC_unixunixnamedstrdnsrequestsuccessclient.md)<br> ↳[unix-unixnamed-str-dns-request-success-rpz](Ps/pC_unixunixnamedstrdnsrequestsuccessrpz.md)<br> ↳[unix-unixnamed-str-dns-request-success-client-1](Ps/pC_unixunixnamedstrdnsrequestsuccessclient1.md)<br> | T1071 - Application Layer Protocol<br>T1568 - Dynamic Resolution<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br>T1583 - T1583<br>T1583.001 - T1583.001<br> | [<ul><li>3 Rules</li></ul>](RM/r_m_unix_unix_named_Malware.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                                                             | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Dynamic Resolution](https://attack.mitre.org/techniques/T1568)<br><br>[Dynamic Resolution: Domain Generation Algorithms](https://attack.mitre.org/techniques/T1568/002)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> |              |        |