Vendor: F5
==========
Product: F5 Advanced Web Application Firewall
---------------------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  18   |   7    |         5          |       1        |    3    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Lateral Movement](../../../UseCases/uc_lateral_movement.md) |  network-traffic:fail (network-connection-failed)<br> ↳[f5-waf-str-network-traffic-fail-warningtmm](Ps/pC_f5wafstrnetworktrafficfailwarningtmm.md)<br> ↳[f5-waf-str-network-traffic-fail-ssl](Ps/pC_f5wafstrnetworktrafficfailssl.md)<br> ↳[f5-waf-str-network-traffic-fail-ssl-1](Ps/pC_f5wafstrnetworktrafficfailssl1.md)<br> | T1090 - Proxy<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1190 - Exploit Public Fasing Application<br>TA0010 - TA0010<br>TA0011 - TA0011<br> | [<ul><li>18 Rules</li></ul><ul><li>7 Models</li></ul>](RM/r_m_f5_f5_advanced_web_application_firewall_Lateral_Movement.md) |
|          [Malware](../../../UseCases/uc_malware.md)          |  network-traffic:fail (network-connection-failed)<br> ↳[f5-waf-str-network-traffic-fail-warningtmm](Ps/pC_f5wafstrnetworktrafficfailwarningtmm.md)<br> ↳[f5-waf-str-network-traffic-fail-ssl](Ps/pC_f5wafstrnetworktrafficfailssl.md)<br> ↳[f5-waf-str-network-traffic-fail-ssl-1](Ps/pC_f5wafstrnetworktrafficfailssl1.md)<br> | TA0011 - TA0011<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_f5_f5_advanced_web_application_firewall_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      |                 |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |