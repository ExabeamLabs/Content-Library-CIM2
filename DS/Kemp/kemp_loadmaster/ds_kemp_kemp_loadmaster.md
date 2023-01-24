Vendor: Kemp
============
Product: Kemp LoadMaster
------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  91   |   46   |     9      |       4        |    4    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  ""app-logout:success""<br> ↳[kemp-loadmaster-str-app-logout-success-loggedout](Ps/pC_kemploadmasterstrapplogoutsuccessloggedout.md)<br><br> ""app-notification:success""<br> ↳[kemp-loadmaster-str-app-notification-disabled](Ps/pC_kemploadmasterstrappnotificationdisabled.md)<br> ↳[kemp-loadmaster-str-app-notification-automatedbackup](Ps/pC_kemploadmasterstrappnotificationautomatedbackup.md)<br> ↳[kemp-loadmaster-str-app-notification-smtpalertsuccessfullysent](Ps/pC_kemploadmasterstrappnotificationsmtpalertsuccessfullysent.md)<br><br> app-activity<br> ↳[kemp-loadmaster-str-app-activity-l4d](Ps/pC_kemploadmasterstrappactivityl4d.md)<br> ↳[kemp-loadmaster-kv-app-activity-success-ssoauthtokenreused](Ps/pC_kemploadmasterkvappactivitysuccessssoauthtokenreused.md)<br><br> dlp-alert<br> ↳[kemp-loadmaster-str-alert-trigger-success-attempted](Ps/pC_kemploadmasterstralerttriggersuccessattempted.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>12 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_kemp_kemp_loadmaster_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  ""app-logout:success""<br> ↳[kemp-loadmaster-str-app-logout-success-loggedout](Ps/pC_kemploadmasterstrapplogoutsuccessloggedout.md)<br><br> ""app-notification:success""<br> ↳[kemp-loadmaster-str-app-notification-disabled](Ps/pC_kemploadmasterstrappnotificationdisabled.md)<br> ↳[kemp-loadmaster-str-app-notification-automatedbackup](Ps/pC_kemploadmasterstrappnotificationautomatedbackup.md)<br> ↳[kemp-loadmaster-str-app-notification-smtpalertsuccessfullysent](Ps/pC_kemploadmasterstrappnotificationsmtpalertsuccessfullysent.md)<br><br> app-activity<br> ↳[kemp-loadmaster-str-app-activity-l4d](Ps/pC_kemploadmasterstrappactivityl4d.md)<br> ↳[kemp-loadmaster-kv-app-activity-success-ssoauthtokenreused](Ps/pC_kemploadmasterkvappactivitysuccessssoauthtokenreused.md)<br><br> dlp-alert<br> ↳[kemp-loadmaster-str-alert-trigger-success-attempted](Ps/pC_kemploadmasterstralerttriggersuccessattempted.md)<br> | T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br> | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_kemp_kemp_loadmaster_Account_Manipulation.md)    |
[Next Page -->>](2_ds_kemp_kemp_loadmaster.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                   | Execution | Persistence                                                                                                                                                                                                                                                                                                                                 | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection                                                                                                                                                            | Command and Control                                                                                                                                                                                                      | Exfiltration                                                                | Impact |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------- | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  | [Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |