Vendor: Microsoft
=================
Product: Web Application Proxy-TLS Gateway
------------------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  75   |   27   |         21         |       2        |    2    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  http-traffic:success (web-activity-allowed)<br> ↳[microsoft-wapgateway-json-http-session-reqid](Ps/pC_microsoftwapgatewayjsonhttpsessionreqid.md)<br> ↳[microsoft-wapgateway-str-http-session-tinet](Ps/pC_microsoftwapgatewaystrhttpsessiontinet.md)<br> ↳[microsoft-wapgateway-kv-http-session-thttp](Ps/pC_microsoftwapgatewaykvhttpsessionthttp.md)<br><br> http-session:fail (web-activity-denied)<br> ↳[microsoft-wapgateway-json-http-session-reqid](Ps/pC_microsoftwapgatewayjsonhttpsessionreqid.md)<br> ↳[microsoft-wapgateway-str-http-session-tinet](Ps/pC_microsoftwapgatewaystrhttpsessiontinet.md)<br> ↳[microsoft-wapgateway-kv-http-session-thttp](Ps/pC_microsoftwapgatewaykvhttpsessionthttp.md)<br> | T1071 - Application Layer Protocol<br>T1071.001 - Application Layer Protocol: Web Protocols<br>    | [<ul><li>6 Rules</li></ul><ul><li>6 Models</li></ul>](RM/r_m_microsoft_web_application_proxy-tls_gateway_Abnormal_Authentication_&_Access.md) |
|          [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md)          |  http-traffic:success (web-activity-allowed)<br> ↳[microsoft-wapgateway-json-http-session-reqid](Ps/pC_microsoftwapgatewayjsonhttpsessionreqid.md)<br> ↳[microsoft-wapgateway-str-http-session-tinet](Ps/pC_microsoftwapgatewaystrhttpsessiontinet.md)<br> ↳[microsoft-wapgateway-kv-http-session-thttp](Ps/pC_microsoftwapgatewaykvhttpsessionthttp.md)<br><br> http-session:fail (web-activity-denied)<br> ↳[microsoft-wapgateway-json-http-session-reqid](Ps/pC_microsoftwapgatewayjsonhttpsessionreqid.md)<br> ↳[microsoft-wapgateway-str-http-session-tinet](Ps/pC_microsoftwapgatewaystrhttpsessiontinet.md)<br> ↳[microsoft-wapgateway-kv-http-session-thttp](Ps/pC_microsoftwapgatewaykvhttpsessionthttp.md)<br> | T1071 - Application Layer Protocol<br>T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>T1102 - Web Service<br>T1189 - Drive-by Compromise<br>T1190 - Exploit Public Fasing Application<br>T1204 - User Execution<br>T1204.001 - T1204.001<br>T1566 - Phishing<br>T1566.002 - Phishing: Spearphishing Link<br>T1568 - Dynamic Resolution<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br> | [<ul><li>40 Rules</li></ul><ul><li>22 Models</li></ul>](RM/r_m_microsoft_web_application_proxy-tls_gateway_Compromised_Credentials.md)        |
|    [Workforce Protection](../../../UseCases/uc_workforce_protection.md)    |  http-traffic:success (web-activity-allowed)<br> ↳[microsoft-wapgateway-json-http-session-reqid](Ps/pC_microsoftwapgatewayjsonhttpsessionreqid.md)<br> ↳[microsoft-wapgateway-str-http-session-tinet](Ps/pC_microsoftwapgatewaystrhttpsessiontinet.md)<br> ↳[microsoft-wapgateway-kv-http-session-thttp](Ps/pC_microsoftwapgatewaykvhttpsessionthttp.md)<br>    | T1071 - Application Layer Protocol<br>T1071.001 - Application Layer Protocol: Web Protocols<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_microsoft_web_application_proxy-tls_gateway_Workforce_Protection.md)    |
[Next Page -->>](2_ds_microsoft_web_application_proxy-tls_gateway.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                                                                                                                                                                                                                                                                                                                      | Execution                                                           | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement                                                            | Collection | Command and Control                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Exfiltration                                                                                                                                                                                                                                                                             | Impact                                                                  |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | --------------------------------------------------------------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| [Phishing: Spearphishing Link](https://attack.mitre.org/techniques/T1566/002)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Drive-by Compromise](https://attack.mitre.org/techniques/T1189)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br>[Phishing](https://attack.mitre.org/techniques/T1566)<br><br> | [User Execution](https://attack.mitre.org/techniques/T1204)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           | [Internal Spearphishing](https://attack.mitre.org/techniques/T1534)<br><br> |            | [Web Service](https://attack.mitre.org/techniques/T1102)<br><br>[Application Layer Protocol: Web Protocols](https://attack.mitre.org/techniques/T1071/001)<br><br>[Dynamic Resolution](https://attack.mitre.org/techniques/T1568)<br><br>[Dynamic Resolution: Domain Generation Algorithms](https://attack.mitre.org/techniques/T1568/002)<br><br>[Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> | [Exfiltration Over C2 Channel](https://attack.mitre.org/techniques/T1041)<br><br>[Exfiltration Over Web Service: Exfiltration to Cloud Storage](https://attack.mitre.org/techniques/T1567/002)<br><br>[Exfiltration Over Web Service](https://attack.mitre.org/techniques/T1567)<br><br> | [Resource Hijacking](https://attack.mitre.org/techniques/T1496)<br><br> |