Vendor: Microsoft
=================
Product: Event Viewer - NTLM
----------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   5   |   3    |     3      |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  authentication-failed<br> ↳[microsoft-evntlm-str-app-authentication-fail-8006](Ps/pC_microsoftevntlmstrappauthenticationfail8006.md)<br> ↳[microsoft-evntlm-str-app-authentication-fail-8005](Ps/pC_microsoftevntlmstrappauthenticationfail8005.md)<br> ↳[microsoft-evntlm-str-app-authentication-fail-8004](Ps/pC_microsoftevntlmstrappauthenticationfail8004.md)<br><br> nac-failed-logon<br> ↳[microsoft-evntlm-kv-endpoint-login-fail-8004](Ps/pC_microsoftevntlmkvendpointloginfail8004.md)<br> | T1133 - External Remote Services<br>    | [<ul><li>3 Rules</li></ul><ul><li>3 Models</li></ul>](RM/r_m_microsoft_event_viewer_-_ntlm_Abnormal_Authentication_&_Access.md) |
|    [Lateral Movement](../../../UseCases/uc_lateral_movement.md)    |  authentication-failed<br> ↳[microsoft-evntlm-str-app-authentication-fail-8006](Ps/pC_microsoftevntlmstrappauthenticationfail8006.md)<br> ↳[microsoft-evntlm-str-app-authentication-fail-8005](Ps/pC_microsoftevntlmstrappauthenticationfail8005.md)<br> ↳[microsoft-evntlm-str-app-authentication-fail-8004](Ps/pC_microsoftevntlmstrappauthenticationfail8004.md)<br><br> nac-failed-logon<br> ↳[microsoft-evntlm-kv-endpoint-login-fail-8004](Ps/pC_microsoftevntlmkvendpointloginfail8004.md)<br> | T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_event_viewer_-_ntlm_Lateral_Movement.md)    |
|    [Ransomware](../../../UseCases/uc_ransomware.md)    |  authentication-failed<br> ↳[microsoft-evntlm-str-app-authentication-fail-8006](Ps/pC_microsoftevntlmstrappauthenticationfail8006.md)<br> ↳[microsoft-evntlm-str-app-authentication-fail-8005](Ps/pC_microsoftevntlmstrappauthenticationfail8005.md)<br> ↳[microsoft-evntlm-str-app-authentication-fail-8004](Ps/pC_microsoftevntlmstrappauthenticationfail8004.md)<br><br> nac-failed-logon<br> ↳[microsoft-evntlm-kv-endpoint-login-fail-8004](Ps/pC_microsoftevntlmkvendpointloginfail8004.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_event_viewer_-_ntlm_Ransomware.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                   | Execution | Persistence                                                                                                                                      | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |