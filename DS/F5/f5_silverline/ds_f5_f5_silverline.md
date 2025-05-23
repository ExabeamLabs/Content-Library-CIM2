Vendor: F5
==========
Product: F5 Silverline
----------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  43   |   18   |         8          |       2        |    5    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  alert-trigger:success (network-alert)<br> ↳[f5-silverline-json-alert-trigger-success-waf](Ps/pC_f5silverlinejsonalerttriggersuccesswaf.md)<br> ↳[f5-silverline-kv-alert-trigger-ipi](Ps/pC_f5silverlinekvalerttriggeripi.md)<br> ↳[f5-silverline-kv-alert-trigger-ipi-1](Ps/pC_f5silverlinekvalerttriggeripi1.md)<br> ↳[f5-silverline-csv-alert-trigger-l7ddos](Ps/pC_f5silverlinecsvalerttriggerl7ddos.md)<br> ↳[f5-silverline-json-alert-trigger-success-waf](Ps/pC_f5silverlinejsonalerttriggersuccesswaf.md)<br> | T1027 - Obfuscated Files or Information<br>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>T1190 - Exploit Public Fasing Application<br> | [<ul><li>21 Rules</li></ul><ul><li>9 Models</li></ul>](RM/r_m_f5_f5_silverline_Compromised_Credentials.md) |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  network-traffic:fail (network-connection-failed)<br> ↳[f5-silverline-kv-network-session-fail-irule](Ps/pC_f5silverlinekvnetworksessionfailirule.md)<br>    | T1090 - Proxy<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1190 - Exploit Public Fasing Application<br>TA0010 - TA0010<br>TA0011 - TA0011<br>    | [<ul><li>18 Rules</li></ul><ul><li>7 Models</li></ul>](RM/r_m_f5_f5_silverline_Lateral_Movement.md)        |
[Next Page -->>](2_ds_f5_f5_silverline.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion                                                                                                                                                                                            | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      | [Obfuscated Files or Information: Indicator Removal from Tools](https://attack.mitre.org/techniques/T1027/005)<br><br>[Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027)<br><br> |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |