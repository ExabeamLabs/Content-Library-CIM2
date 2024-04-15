Vendor: Arbor
=============
Product: Arbor Cloud
--------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  27   |   10   |         6          |       1        |    0    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
|     [Cryptomining](../../../UseCases/uc_cryptomining.md)     |  network-connection-failed<br> ↳[arbor-a-str-network-traffic-fail-block](Ps/pC_arborastrnetworktrafficfailblock.md)<br> | T1496 - Resource Hijacking<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_arbor_arbor_cloud_Cryptomining.md)    |
| [Lateral Movement](../../../UseCases/uc_lateral_movement.md) |  network-connection-failed<br> ↳[arbor-a-str-network-traffic-fail-block](Ps/pC_arborastrnetworktrafficfailblock.md)<br> | T1048 - Exfiltration Over Alternative Protocol<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1190 - Exploit Public Fasing Application<br>TA0010 - TA0010<br>TA0011 - TA0011<br> | [<ul><li>25 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_arbor_arbor_cloud_Lateral_Movement.md) |
|          [Malware](../../../UseCases/uc_malware.md)          |  network-connection-failed<br> ↳[arbor-a-str-network-traffic-fail-block](Ps/pC_arborastrnetworktrafficfailblock.md)<br> | TA0011 - TA0011<br>    | [<ul><li>3 Rules</li></ul>](RM/r_m_arbor_arbor_cloud_Malware.md)    |
|       [Ransomware](../../../UseCases/uc_ransomware.md)       |  network-connection-failed<br> ↳[arbor-a-str-network-traffic-fail-block](Ps/pC_arborastrnetworktrafficfailblock.md)<br> | TA0011 - TA0011<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_arbor_arbor_cloud_Ransomware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration                                                                                | Impact                                                                  |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      |                 |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> | [Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048)<br><br> | [Resource Hijacking](https://attack.mitre.org/techniques/T1496)<br><br> |