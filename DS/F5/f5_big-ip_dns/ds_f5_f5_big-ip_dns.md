Vendor: F5
==========
Product: F5 BIG-IP DNS
----------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   0    |         5          |       2        |    3    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Malware](../../../UseCases/uc_malware.md) |  dns-request:success (dns-query)<br> ↳[f5-bigipdns-kv-dns-request-response-success-dns](Ps/pC_f5bigipdnskvdnsrequestresponsesuccessdns.md)<br> ↳[f5-bigipdns-str-dns-request-success-qid](Ps/pC_f5bigipdnsstrdnsrequestsuccessqid.md)<br><br> dns-response:success (dns-response)<br> ↳[f5-bigipdns-kv-dns-request-response-success-dns](Ps/pC_f5bigipdnskvdnsrequestresponsesuccessdns.md)<br> ↳[f5-bigipdns-str-dns-response-success-rcode](Ps/pC_f5bigipdnsstrdnsresponsesuccessrcode.md)<br> ↳[f5-bigipdns-str-dns-response-success-to](Ps/pC_f5bigipdnsstrdnsresponsesuccessto.md)<br> | T1071 - Application Layer Protocol<br>T1568 - Dynamic Resolution<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br>T1583 - T1583<br>T1583.001 - T1583.001<br> | [<ul><li>5 Rules</li></ul>](RM/r_m_f5_f5_big-ip_dns_Malware.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                                                             | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Dynamic Resolution](https://attack.mitre.org/techniques/T1568)<br><br>[Dynamic Resolution: Domain Generation Algorithms](https://attack.mitre.org/techniques/T1568/002)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> |              |        |