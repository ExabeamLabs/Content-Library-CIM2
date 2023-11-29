Vendor: Microsoft
=================
Product: Event Viewer - NPS
---------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  12   |   6    |         2          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  nac-logon<br> ↳[microsoft-evnps-sk4-endpoint-authentication-success-6272](Ps/pC_microsoftevnpssk4endpointauthenticationsuccess6272.md)<br> ↳[microsoft-evnps-sk4-endpoint-authentication-success-6272-1](Ps/pC_microsoftevnpssk4endpointauthenticationsuccess62721.md)<br> | T1021 - Remote Services<br>T1078 - Valid Accounts<br> | [<ul><li>8 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_microsoft_event_viewer_-_nps_Abnormal_Authentication_&_Access.md) |
|          [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md)          |  nac-logon<br> ↳[microsoft-evnps-sk4-endpoint-authentication-success-6272](Ps/pC_microsoftevnpssk4endpointauthenticationsuccess6272.md)<br> ↳[microsoft-evnps-sk4-endpoint-authentication-success-6272-1](Ps/pC_microsoftevnpssk4endpointauthenticationsuccess62721.md)<br> | T1021 - Remote Services<br>T1078 - Valid Accounts<br> | [<ul><li>6 Rules</li></ul><ul><li>3 Models</li></ul>](RM/r_m_microsoft_event_viewer_-_nps_Compromised_Credentials.md)          |
|    [Lateral Movement](../../../UseCases/uc_lateral_movement.md)    |  nac-logon<br> ↳[microsoft-evnps-sk4-endpoint-authentication-success-6272](Ps/pC_microsoftevnpssk4endpointauthenticationsuccess6272.md)<br> ↳[microsoft-evnps-sk4-endpoint-authentication-success-6272-1](Ps/pC_microsoftevnpssk4endpointauthenticationsuccess62721.md)<br> | T1021 - Remote Services<br>T1078 - Valid Accounts<br> | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_microsoft_event_viewer_-_nps_Lateral_Movement.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement                                                     | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | -------------------------------------------------------------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           | [Remote Services](https://attack.mitre.org/techniques/T1021)<br><br> |            |                     |              |        |