Vendor: Splunk
==============
Product: Splunk Stream
----------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   0    |         5          |       2        |    2    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Malware](../../../UseCases/uc_malware.md) |  dns-request:success (dns-query)<br> ↳[splunk-stream-json-dns-request-success-query](Ps/pC_splunkstreamjsondnsrequestsuccessquery.md)<br><br> dns-response:success (dns-response)<br> ↳[splunk-stream-json-dns-response-success-messagetype](Ps/pC_splunkstreamjsondnsresponsesuccessmessagetype.md)<br> | T1071 - Application Layer Protocol<br>T1568 - Dynamic Resolution<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br>T1583 - T1583<br>T1583.001 - T1583.001<br> | [<ul><li>5 Rules</li></ul>](RM/r_m_splunk_splunk_stream_Malware.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                                                             | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Dynamic Resolution](https://attack.mitre.org/techniques/T1568)<br><br>[Dynamic Resolution: Domain Generation Algorithms](https://attack.mitre.org/techniques/T1568/002)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> |              |        |