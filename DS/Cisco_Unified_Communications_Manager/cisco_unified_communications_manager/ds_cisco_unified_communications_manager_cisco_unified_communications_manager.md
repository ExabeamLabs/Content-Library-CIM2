Vendor: Cisco Unified Communications Manager
============================================
Product: Cisco Unified Communications Manager
---------------------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  40   |   17   |     4      |       4        |    4    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  ""app-notification:success""<br> ↳[cisco-ucm-kv-app-notification-success-deviceupdate](Ps/pC_ciscoucmkvappnotificationsuccessdeviceupdate.md)<br><br> ""user-role-modify:success""<br> ↳[cisco-ucm-kv-user-role-modify-success-userrolemembershipupdate](Ps/pC_ciscoucmkvuserrolemodifysuccessuserrolemembershipupdate.md)<br><br> app-login<br> ↳[cisco-ucm-kv-app-login-success-userlogging](Ps/pC_ciscoucmkvapploginsuccessuserlogging.md)<br><br> config-change<br> ↳[cisco-ucm-kv-configuration-modify-success-generalconfigurationupdate](Ps/pC_ciscoucmkvconfigurationmodifysuccessgeneralconfigurationupdate.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>12 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_cisco_unified_communications_manager_cisco_unified_communications_manager_Abnormal_Authentication_&_Access.md) |
|          [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md)          |  ""app-notification:success""<br> ↳[cisco-ucm-kv-app-notification-success-deviceupdate](Ps/pC_ciscoucmkvappnotificationsuccessdeviceupdate.md)<br><br> ""user-role-modify:success""<br> ↳[cisco-ucm-kv-user-role-modify-success-userrolemembershipupdate](Ps/pC_ciscoucmkvuserrolemodifysuccessuserrolemembershipupdate.md)<br><br> app-login<br> ↳[cisco-ucm-kv-app-login-success-userlogging](Ps/pC_ciscoucmkvapploginsuccessuserlogging.md)<br><br> config-change<br> ↳[cisco-ucm-kv-configuration-modify-success-generalconfigurationupdate](Ps/pC_ciscoucmkvconfigurationmodifysuccessgeneralconfigurationupdate.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>T1190 - Exploit Public Fasing Application<br> | [<ul><li>27 Rules</li></ul><ul><li>16 Models</li></ul>](RM/r_m_cisco_unified_communications_manager_cisco_unified_communications_manager_Compromised_Credentials.md)         |
[Next Page -->>](2_ds_cisco_unified_communications_manager_cisco_unified_communications_manager.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                      | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |