Vendor: VMware
==============
Product: NSX Distributed Firewall
---------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  56   |   20   |         6          |       2        |    0    |

|    Use-Case    | Activity Types(Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Lateral Movement](../../../UseCases/uc_lateral_movement.md) |  network-traffic:fail(network-connection-failed)<br> ↳[vmware-nsxfw-cef-network-traffic-success-nsxfw](Ps/pC_vmwarensxfwcefnetworktrafficsuccessnsxfw.md)<br><br> network-traffic:success(network-connection-successful)<br> ↳[vmware-nsxfw-cef-network-traffic-success-nsxfw](Ps/pC_vmwarensxfwcefnetworktrafficsuccessnsxfw.md)<br> | T1071 - Application Layer Protocol<br>T1090 - Proxy<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1190 - Exploit Public Fasing Application<br>TA0010 - TA0010<br>TA0011 - TA0011<br> | [<ul><li>56 Rules</li></ul><ul><li>20 Models</li></ul>](RM/r_m_vmware_nsx_distributed_firewall_Lateral_Movement.md) |
|          [Malware](../../../UseCases/uc_malware.md)          |  network-traffic:fail(network-connection-failed)<br> ↳[vmware-nsxfw-cef-network-traffic-success-nsxfw](Ps/pC_vmwarensxfwcefnetworktrafficsuccessnsxfw.md)<br><br> network-traffic:success(network-connection-successful)<br> ↳[vmware-nsxfw-cef-network-traffic-success-nsxfw](Ps/pC_vmwarensxfwcefnetworktrafficsuccessnsxfw.md)<br> | TA0011 - TA0011<br>    | [<ul><li>4 Rules</li></ul>](RM/r_m_vmware_nsx_distributed_firewall_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                      | Exfiltration | Impact |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | ------ |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      |                 |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |