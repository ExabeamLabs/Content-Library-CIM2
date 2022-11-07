Vendor: ESector
===============
Product: ESector DEFESA
-----------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  109  |   45   |     17     |       6        |    6    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  ""app-logout:success""<br> ↳[esector-defesa-json-app-logout-success-applogout](Ps/pC_esectordefesajsonapplogoutsuccessapplogout.md)<br><br> app-activity<br> ↳[esector-defesa-json-app-activity-appactivity](Ps/pC_esectordefesajsonappactivityappactivity.md)<br><br> app-login<br> ↳[esector-defesa-json-app-login-success-applogin](Ps/pC_esectordefesajsonapploginsuccessapplogin.md)<br><br> file-delete<br> ↳[esector-defesa-json-file-delete-success-user](Ps/pC_esectordefesajsonfiledeletesuccessuser.md)<br><br> file-read<br> ↳[esector-defesa-json-file-read-success-user](Ps/pC_esectordefesajsonfilereadsuccessuser.md)<br><br> file-write<br> ↳[esector-defesa-json-file-write-success-user](Ps/pC_esectordefesajsonfilewritesuccessuser.md)<br> ↳[esector-defesa-json-file-write-success-user-2](Ps/pC_esectordefesajsonfilewritesuccessuser2.md)<br> ↳[esector-defesa-json-file-write-success-user-1](Ps/pC_esectordefesajsonfilewritesuccessuser1.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>12 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_esector_esector_defesa_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  ""app-logout:success""<br> ↳[esector-defesa-json-app-logout-success-applogout](Ps/pC_esectordefesajsonapplogoutsuccessapplogout.md)<br><br> app-activity<br> ↳[esector-defesa-json-app-activity-appactivity](Ps/pC_esectordefesajsonappactivityappactivity.md)<br><br> app-login<br> ↳[esector-defesa-json-app-login-success-applogin](Ps/pC_esectordefesajsonapploginsuccessapplogin.md)<br><br> file-delete<br> ↳[esector-defesa-json-file-delete-success-user](Ps/pC_esectordefesajsonfiledeletesuccessuser.md)<br><br> file-read<br> ↳[esector-defesa-json-file-read-success-user](Ps/pC_esectordefesajsonfilereadsuccessuser.md)<br><br> file-write<br> ↳[esector-defesa-json-file-write-success-user](Ps/pC_esectordefesajsonfilewritesuccessuser.md)<br> ↳[esector-defesa-json-file-write-success-user-2](Ps/pC_esectordefesajsonfilewritesuccessuser2.md)<br> ↳[esector-defesa-json-file-write-success-user-1](Ps/pC_esectordefesajsonfilewritesuccessuser1.md)<br> | T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br> | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_esector_esector_defesa_Account_Manipulation.md)    |
[Next Page -->>](2_ds_esector_esector_defesa.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Privilege Escalation                                                                                                                                      | Defense Evasion                                                                                                                                                                                                                                    | Credential Access                                                          | Discovery                                                                         | Lateral Movement | Collection                                                                                                                                                            | Command and Control                                                                                                                       | Exfiltration | Impact                                                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Server Software Component: Web Shell](https://attack.mitre.org/techniques/T1505/003)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Server Software Component](https://attack.mitre.org/techniques/T1505)<br><br>[Boot or Logon Autostart Execution](https://attack.mitre.org/techniques/T1547)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Boot or Logon Autostart Execution](https://attack.mitre.org/techniques/T1547)<br><br> | [Indicator Removal on Host: File Deletion](https://attack.mitre.org/techniques/T1070/004)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Indicator Removal on Host](https://attack.mitre.org/techniques/T1070)<br><br> | [OS Credential Dumping](https://attack.mitre.org/techniques/T1003)<br><br> | [File and Directory Discovery](https://attack.mitre.org/techniques/T1083)<br><br> |                  | [Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              | [Data Destruction](https://attack.mitre.org/techniques/T1485)<br><br>[Data Encrypted for Impact](https://attack.mitre.org/techniques/T1486)<br><br> |