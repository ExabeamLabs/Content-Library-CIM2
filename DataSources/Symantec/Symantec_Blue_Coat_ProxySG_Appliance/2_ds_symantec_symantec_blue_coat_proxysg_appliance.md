|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
|         [Cryptomining](../../../UseCases/uc_cryptomining.md)         |  network-connection-failed<br> ↳[symantec-bcpa-str-network-traffic-fail-tcp](Ps/pC_symantecbcpastrnetworktrafficfailtcp.md)<br> ↳[symantec-bcpa-str-network-traffic-fail-ssl](Ps/pC_symantecbcpastrnetworktrafficfailssl.md)<br><br> web-activity-allowed<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br><br> web-activity-denied<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>T1496 - Resource Hijacking<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_symantec_symantec_blue_coat_proxysg_appliance_Cryptomining.md)    |
|    [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)    |  network-connection-failed<br> ↳[symantec-bcpa-str-network-traffic-fail-tcp](Ps/pC_symantecbcpastrnetworktrafficfailtcp.md)<br> ↳[symantec-bcpa-str-network-traffic-fail-ssl](Ps/pC_symantecbcpastrnetworktrafficfailssl.md)<br><br> web-activity-allowed<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br><br> web-activity-denied<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br> | T1041 - Exfiltration Over C2 Channel<br>T1071.001 - Application Layer Protocol: Web Protocols<br>T1567 - Exfiltration Over Web Service<br>T1567.002 - Exfiltration Over Web Service: Exfiltration to Cloud Storage<br>T1568 - Dynamic Resolution<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br> | [<ul><li>8 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_symantec_symantec_blue_coat_proxysg_appliance_Data_Exfiltration.md)    |
|    [Data Leak](../../../UseCases/uc_data_leak.md)    |  network-connection-failed<br> ↳[symantec-bcpa-str-network-traffic-fail-tcp](Ps/pC_symantecbcpastrnetworktrafficfailtcp.md)<br> ↳[symantec-bcpa-str-network-traffic-fail-ssl](Ps/pC_symantecbcpastrnetworktrafficfailssl.md)<br><br> web-activity-allowed<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br><br> web-activity-denied<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br> | T1041 - Exfiltration Over C2 Channel<br>T1071.001 - Application Layer Protocol: Web Protocols<br>T1567 - Exfiltration Over Web Service<br>T1567.002 - Exfiltration Over Web Service: Exfiltration to Cloud Storage<br>    | [<ul><li>6 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_symantec_symantec_blue_coat_proxysg_appliance_Data_Leak.md)    |
|     [Lateral Movement](../../../UseCases/uc_lateral_movement.md)     |  network-connection-failed<br> ↳[symantec-bcpa-str-network-traffic-fail-tcp](Ps/pC_symantecbcpastrnetworktrafficfailtcp.md)<br> ↳[symantec-bcpa-str-network-traffic-fail-ssl](Ps/pC_symantecbcpastrnetworktrafficfailssl.md)<br><br> web-activity-allowed<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br><br> web-activity-denied<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1190 - Exploit Public Fasing Application<br>TA0010 - TA0010<br>TA0011 - TA0011<br>    | [<ul><li>26 Rules</li></ul><ul><li>7 Models</li></ul>](RM/r_m_symantec_symantec_blue_coat_proxysg_appliance_Lateral_Movement.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  network-connection-failed<br> ↳[symantec-bcpa-str-network-traffic-fail-tcp](Ps/pC_symantecbcpastrnetworktrafficfailtcp.md)<br> ↳[symantec-bcpa-str-network-traffic-fail-ssl](Ps/pC_symantecbcpastrnetworktrafficfailssl.md)<br><br> web-activity-allowed<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br><br> web-activity-denied<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>T1189 - Drive-by Compromise<br>T1190 - Exploit Public Fasing Application<br>T1204.001 - T1204.001<br>T1566.002 - Phishing: Spearphishing Link<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br>TA0011 - TA0011<br>    | [<ul><li>26 Rules</li></ul><ul><li>7 Models</li></ul>](RM/r_m_symantec_symantec_blue_coat_proxysg_appliance_Malware.md)    |
|    [Phishing](../../../UseCases/uc_phishing.md)    |  network-connection-failed<br> ↳[symantec-bcpa-str-network-traffic-fail-tcp](Ps/pC_symantecbcpastrnetworktrafficfailtcp.md)<br> ↳[symantec-bcpa-str-network-traffic-fail-ssl](Ps/pC_symantecbcpastrnetworktrafficfailssl.md)<br><br> web-activity-allowed<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br><br> web-activity-denied<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br> | T1189 - Drive-by Compromise<br>T1204.001 - T1204.001<br>T1534 - Internal Spearphishing<br>T1566.002 - Phishing: Spearphishing Link<br>T1598.003 - T1598.003<br>    | [<ul><li>4 Rules</li></ul>](RM/r_m_symantec_symantec_blue_coat_proxysg_appliance_Phishing.md)    |
|      [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)      |  network-connection-failed<br> ↳[symantec-bcpa-str-network-traffic-fail-tcp](Ps/pC_symantecbcpastrnetworktrafficfailtcp.md)<br> ↳[symantec-bcpa-str-network-traffic-fail-ssl](Ps/pC_symantecbcpastrnetworktrafficfailssl.md)<br><br> web-activity-allowed<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br><br> web-activity-denied<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_symantec_symantec_blue_coat_proxysg_appliance_Privilege_Abuse.md)    |
|  [Privileged Activity](../../../UseCases/uc_privileged_activity.md)  |  network-connection-failed<br> ↳[symantec-bcpa-str-network-traffic-fail-tcp](Ps/pC_symantecbcpastrnetworktrafficfailtcp.md)<br> ↳[symantec-bcpa-str-network-traffic-fail-ssl](Ps/pC_symantecbcpastrnetworktrafficfailssl.md)<br><br> web-activity-allowed<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br><br> web-activity-denied<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>T1102 - Web Service<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_symantec_symantec_blue_coat_proxysg_appliance_Privileged_Activity.md)    |
|    [Ransomware](../../../UseCases/uc_ransomware.md)    |  network-connection-failed<br> ↳[symantec-bcpa-str-network-traffic-fail-tcp](Ps/pC_symantecbcpastrnetworktrafficfailtcp.md)<br> ↳[symantec-bcpa-str-network-traffic-fail-ssl](Ps/pC_symantecbcpastrnetworktrafficfailssl.md)<br><br> web-activity-allowed<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br><br> web-activity-denied<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_symantec_symantec_blue_coat_proxysg_appliance_Ransomware.md)    |
| [Workforce Protection](../../../UseCases/uc_workforce_protection.md) |  network-connection-failed<br> ↳[symantec-bcpa-str-network-traffic-fail-tcp](Ps/pC_symantecbcpastrnetworktrafficfailtcp.md)<br> ↳[symantec-bcpa-str-network-traffic-fail-ssl](Ps/pC_symantecbcpastrnetworktrafficfailssl.md)<br><br> web-activity-allowed<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br><br> web-activity-denied<br> ↳[symantec-bcpa-cef-http-session-proxysg](Ps/pC_symantecbcpacefhttpsessionproxysg.md)<br> ↳[symantec-bcpa-space-delimited-http-session-proxied](Ps/pC_symantecbcpaspacedelimitedhttpsessionproxied.md)<br> ↳[symantec-bcpa-json-http-session-queryresponse](Ps/pC_symantecbcpajsonhttpsessionqueryresponse.md)<br> | T1071.001 - Application Layer Protocol: Web Protocols<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_symantec_symantec_blue_coat_proxysg_appliance_Workforce_Protection.md) |