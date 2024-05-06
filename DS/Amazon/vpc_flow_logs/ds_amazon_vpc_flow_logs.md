Vendor: Amazon
==============
Product: VPC Flow Logs
----------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  39   |   17   |         5          |       1        |    3    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Lateral Movement](../../../UseCases/uc_lateral_movement.md) |  network-connection-successful<br> ↳[amazon-awsvpc-str-network-traffic-success-accept](Ps/pC_amazonawsvpcstrnetworktrafficsuccessaccept.md)<br> ↳[amazon-awsvpc-str-network-traffic-fail-reject](Ps/pC_amazonawsvpcstrnetworktrafficfailreject.md)<br> ↳[amazon-awsvpc-str-network-notification-success-skipdata](Ps/pC_amazonawsvpcstrnetworknotificationsuccessskipdata.md)<br> ↳[amazon-awsvpc-str-network-notification-success-nodata](Ps/pC_amazonawsvpcstrnetworknotificationsuccessnodata.md)<br> | T1071 - Application Layer Protocol<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1190 - Exploit Public Fasing Application<br>TA0010 - TA0010<br>TA0011 - TA0011<br> | [<ul><li>39 Rules</li></ul><ul><li>17 Models</li></ul>](RM/r_m_amazon_vpc_flow_logs_Lateral_Movement.md) |
|          [Malware](../../../UseCases/uc_malware.md)          |  network-connection-successful<br> ↳[amazon-awsvpc-str-network-traffic-success-accept](Ps/pC_amazonawsvpcstrnetworktrafficsuccessaccept.md)<br> ↳[amazon-awsvpc-str-network-traffic-fail-reject](Ps/pC_amazonawsvpcstrnetworktrafficfailreject.md)<br> ↳[amazon-awsvpc-str-network-notification-success-skipdata](Ps/pC_amazonawsvpcstrnetworknotificationsuccessskipdata.md)<br> ↳[amazon-awsvpc-str-network-notification-success-nodata](Ps/pC_amazonawsvpcstrnetworknotificationsuccessnodata.md)<br> | TA0011 - TA0011<br>    | [<ul><li>3 Rules</li></ul>](RM/r_m_amazon_vpc_flow_logs_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                      | Exfiltration | Impact |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | ------ |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      |                 |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |