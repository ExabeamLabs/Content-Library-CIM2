Vendor: Infoblox
================
Product: BloxOne
----------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   5   |   0    |     3      |       3        |    3    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Malware](../../../UseCases/uc_malware.md) |  computer-logon<br> ↳[infoblox-bloxone-kv-endpoint-login-success-loginallowed](Ps/pC_infobloxbloxonekvendpointloginsuccessloginallowed.md)<br> ↳[infoblox-bloxone-str-dhcp-traffic-success-dynamicleases](Ps/pC_infobloxbloxonestrdhcptrafficsuccessdynamicleases.md)<br><br> dns-query<br> ↳[infoblox-bloxone-csv-dns-request-success-query](Ps/pC_infobloxbloxonecsvdnsrequestsuccessquery.md)<br><br> dns-response<br> ↳[infoblox-bloxone-csv-dns-response-success-response](Ps/pC_infobloxbloxonecsvdnsresponsesuccessresponse.md)<br> | T1071 - Application Layer Protocol<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br>T1583.001 - T1583.001<br> | [<ul><li>5 Rules</li></ul>](RM/r_m_infoblox_bloxone_Malware.md) |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                                                             | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Dynamic Resolution](https://attack.mitre.org/techniques/T1568)<br><br>[Dynamic Resolution: Domain Generation Algorithms](https://attack.mitre.org/techniques/T1568/002)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> |              |        |