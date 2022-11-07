Vendor: Bitglass
================
Product: Bitglass CASB
----------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  129  |   54   |     10     |       5        |    5    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  ""app-scan:success""<br> ↳[bitglass-casb-cef-app-scan-malwarescan](Ps/pC_bitglasscasbcefappscanmalwarescan.md)<br> ↳[bitglass-casb-cef-app-scan-dlpscan](Ps/pC_bitglasscasbcefappscandlpscan.md)<br> ↳[bitglass-casb-cef-app-scan-scantimeout](Ps/pC_bitglasscasbcefappscanscantimeout.md)<br><br> app-activity<br> ↳[bitglass-casb-sk4-app-activity-success-onedrive](Ps/pC_bitglasscasbsk4appactivitysuccessonedrive.md)<br><br> app-login<br> ↳[bitglass-casb-sk4-app-login-success-loginsuccess](Ps/pC_bitglasscasbsk4apploginsuccessloginsuccess.md)<br><br> dlp-email-alert-out<br> ↳[bitglass-casb-json-email-send-success-emailsend](Ps/pC_bitglasscasbjsonemailsendsuccessemailsend.md)<br><br> security-alert<br> ↳[bitglass-casb-cef-alert-trigger-success-filelink](Ps/pC_bitglasscasbcefalerttriggersuccessfilelink.md)<br> ↳[bitglass-casb-sk4-alert-trigger-success-cloudsummary](Ps/pC_bitglasscasbsk4alerttriggersuccesscloudsummary.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>12 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_bitglass_bitglass_casb_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  ""app-scan:success""<br> ↳[bitglass-casb-cef-app-scan-malwarescan](Ps/pC_bitglasscasbcefappscanmalwarescan.md)<br> ↳[bitglass-casb-cef-app-scan-dlpscan](Ps/pC_bitglasscasbcefappscandlpscan.md)<br> ↳[bitglass-casb-cef-app-scan-scantimeout](Ps/pC_bitglasscasbcefappscanscantimeout.md)<br><br> app-activity<br> ↳[bitglass-casb-sk4-app-activity-success-onedrive](Ps/pC_bitglasscasbsk4appactivitysuccessonedrive.md)<br><br> app-login<br> ↳[bitglass-casb-sk4-app-login-success-loginsuccess](Ps/pC_bitglasscasbsk4apploginsuccessloginsuccess.md)<br><br> dlp-email-alert-out<br> ↳[bitglass-casb-json-email-send-success-emailsend](Ps/pC_bitglasscasbjsonemailsendsuccessemailsend.md)<br><br> security-alert<br> ↳[bitglass-casb-cef-alert-trigger-success-filelink](Ps/pC_bitglasscasbcefalerttriggersuccessfilelink.md)<br> ↳[bitglass-casb-sk4-alert-trigger-success-cloudsummary](Ps/pC_bitglasscasbsk4alerttriggersuccesscloudsummary.md)<br> | T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br> | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_bitglass_bitglass_casb_Account_Manipulation.md)    |
[Next Page -->>](2_ds_bitglass_bitglass_casb.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                                                                                                                                                                                                                 | Privilege Escalation                                                                                                                                          | Defense Evasion                                                                                                                                                                                                                                                               | Credential Access | Discovery | Lateral Movement | Collection                                                                                                                                                            | Command and Control                                                                                                                       | Exfiltration                                                                                                                                                                                                                                         | Impact |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068)<br><br> | [Obfuscated Files or Information: Indicator Removal from Tools](https://attack.mitre.org/techniques/T1027/005)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027)<br><br> |                   |           |                  | [Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> | [Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048)<br><br>[Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol](https://attack.mitre.org/techniques/T1048/003)<br><br> |        |