Vendor: Cisco
=============
Product: cisco secure endpoint
------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  32   |   12   |     6      |       3        |    3    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  ""app-notification:success""<br> ↳[cisco-secureendpoint-sk4-app-notification-success-rebootpending](Ps/pC_ciscosecureendpointsk4appnotificationsuccessrebootpending.md)<br> ↳[cisco-secureendpoint-sk4-app-notification-success-rebootrequired](Ps/pC_ciscosecureendpointsk4appnotificationsuccessrebootrequired.md)<br> ↳[cisco-secureendpoint-sk4-app-notification-success-updatecompleted](Ps/pC_ciscosecureendpointsk4appnotificationsuccessupdatecompleted.md)<br> ↳[cisco-secureendpoint-sk4-app-notification-success-rebootadvised](Ps/pC_ciscosecureendpointsk4appnotificationsuccessrebootadvised.md)<br> ↳[cisco-secureendpoint-sk4-app-notification-success-installfailure](Ps/pC_ciscosecureendpointsk4appnotificationsuccessinstallfailure.md)<br> ↳[cisco-secureendpoint-sk4-app-notification-success-rebootcompleted](Ps/pC_ciscosecureendpointsk4appnotificationsuccessrebootcompleted.md)<br><br> ""file-restore:success""<br> ↳[cisco-secureendpoint-sk4-file-restore-success-fromquarantine](Ps/pC_ciscosecureendpointsk4filerestoresuccessfromquarantine.md)<br> ↳[cisco-secureendpoint-sk4-file-restore-success-falsepositive](Ps/pC_ciscosecureendpointsk4filerestoresuccessfalsepositive.md)<br><br> security-alert<br> ↳[cisco-secureendpoint-sk4-alert-trigger-success-systemprocessprotected](Ps/pC_ciscosecureendpointsk4alerttriggersuccesssystemprocessprotected.md)<br> ↳[cisco-secureendpoint-sk4-alert-trigger-success-dropperinfection](Ps/pC_ciscosecureendpointsk4alerttriggersuccessdropperinfection.md)<br> | T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>T1078 - Valid Accounts<br>T1133 - External Remote Services<br>T1190 - Exploit Public Fasing Application<br> | [<ul><li>25 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_cisco_cisco_secure_endpoint_Compromised_Credentials.md) |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  ""app-notification:success""<br> ↳[cisco-secureendpoint-sk4-app-notification-success-rebootpending](Ps/pC_ciscosecureendpointsk4appnotificationsuccessrebootpending.md)<br> ↳[cisco-secureendpoint-sk4-app-notification-success-rebootrequired](Ps/pC_ciscosecureendpointsk4appnotificationsuccessrebootrequired.md)<br> ↳[cisco-secureendpoint-sk4-app-notification-success-updatecompleted](Ps/pC_ciscosecureendpointsk4appnotificationsuccessupdatecompleted.md)<br> ↳[cisco-secureendpoint-sk4-app-notification-success-rebootadvised](Ps/pC_ciscosecureendpointsk4appnotificationsuccessrebootadvised.md)<br> ↳[cisco-secureendpoint-sk4-app-notification-success-installfailure](Ps/pC_ciscosecureendpointsk4appnotificationsuccessinstallfailure.md)<br> ↳[cisco-secureendpoint-sk4-app-notification-success-rebootcompleted](Ps/pC_ciscosecureendpointsk4appnotificationsuccessrebootcompleted.md)<br><br> ""file-restore:success""<br> ↳[cisco-secureendpoint-sk4-file-restore-success-fromquarantine](Ps/pC_ciscosecureendpointsk4filerestoresuccessfromquarantine.md)<br> ↳[cisco-secureendpoint-sk4-file-restore-success-falsepositive](Ps/pC_ciscosecureendpointsk4filerestoresuccessfalsepositive.md)<br><br> security-alert<br> ↳[cisco-secureendpoint-sk4-alert-trigger-success-systemprocessprotected](Ps/pC_ciscosecureendpointsk4alerttriggersuccesssystemprocessprotected.md)<br> ↳[cisco-secureendpoint-sk4-alert-trigger-success-dropperinfection](Ps/pC_ciscosecureendpointsk4alerttriggersuccessdropperinfection.md)<br> | T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_cisco_cisco_secure_endpoint_Lateral_Movement.md)    |
[Next Page -->>](2_ds_cisco_cisco_secure_endpoint.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                      | Privilege Escalation                                                                                                                                          | Defense Evasion                                                                                                                                                                                                                                                               | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068)<br><br> | [Obfuscated Files or Information: Indicator Removal from Tools](https://attack.mitre.org/techniques/T1027/005)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027)<br><br> |                   |           |                  |            |                     |              |        |