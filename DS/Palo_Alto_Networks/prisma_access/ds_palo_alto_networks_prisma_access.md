Vendor: Palo Alto Networks
==========================
Product: Prisma Access
----------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  50   |   21   |         6          |       1        |    0    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
|     [Cryptomining](../../../UseCases/uc_cryptomining.md)     |  network-connection-successful<br> ↳[pan-prismaaccess-leef-network-traffic-success-end](Ps/pC_panprismaaccessleefnetworktrafficsuccessend.md)<br> | T1496 - Resource Hijacking<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_palo_alto_networks_prisma_access_Cryptomining.md)    |
| [Lateral Movement](../../../UseCases/uc_lateral_movement.md) |  network-connection-successful<br> ↳[pan-prismaaccess-leef-network-traffic-success-end](Ps/pC_panprismaaccessleefnetworktrafficsuccessend.md)<br> | T1071 - Application Layer Protocol<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1190 - Exploit Public Fasing Application<br>TA0010 - TA0010<br>TA0011 - TA0011<br> | [<ul><li>48 Rules</li></ul><ul><li>21 Models</li></ul>](RM/r_m_palo_alto_networks_prisma_access_Lateral_Movement.md) |
|          [Malware](../../../UseCases/uc_malware.md)          |  network-connection-successful<br> ↳[pan-prismaaccess-leef-network-traffic-success-end](Ps/pC_panprismaaccessleefnetworktrafficsuccessend.md)<br> | TA0011 - TA0011<br>    | [<ul><li>4 Rules</li></ul>](RM/r_m_palo_alto_networks_prisma_access_Malware.md)    |
|       [Ransomware](../../../UseCases/uc_ransomware.md)       |  network-connection-successful<br> ↳[pan-prismaaccess-leef-network-traffic-success-end](Ps/pC_panprismaaccessleefnetworktrafficsuccessend.md)<br> | TA0011 - TA0011<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_palo_alto_networks_prisma_access_Ransomware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                      | Exfiltration | Impact                                                                  |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | ----------------------------------------------------------------------- |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      |                 |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              | [Resource Hijacking](https://attack.mitre.org/techniques/T1496)<br><br> |