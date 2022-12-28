Vendor: Forcepoint Next-Gen Firewall
====================================
Product: Forcepoint Next-Gen Firewall
-------------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  39   |   17   |     5      |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Lateral Movement](../../../UseCases/uc_lateral_movement.md) |  network-connection-successful<br> ↳[forcepoint-ngfw-cef-network-traffic-success-connectionallowed](Ps/pC_forcepointngfwcefnetworktrafficsuccessconnectionallowed.md)<br> | T1071 - Application Layer Protocol<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1190 - Exploit Public Fasing Application<br>TA0010 - TA0010<br>TA0011 - TA0011<br> | [<ul><li>39 Rules</li></ul><ul><li>17 Models</li></ul>](RM/r_m_forcepoint_next-gen_firewall_forcepoint_next-gen_firewall_Lateral_Movement.md) |
|          [Malware](../../../UseCases/uc_malware.md)          |  network-connection-successful<br> ↳[forcepoint-ngfw-cef-network-traffic-success-connectionallowed](Ps/pC_forcepointngfwcefnetworktrafficsuccessconnectionallowed.md)<br> | TA0011 - TA0011<br>    | [<ul><li>3 Rules</li></ul>](RM/r_m_forcepoint_next-gen_firewall_forcepoint_next-gen_firewall_Malware.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                      | Exfiltration | Impact |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | ------ |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      |                 |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |