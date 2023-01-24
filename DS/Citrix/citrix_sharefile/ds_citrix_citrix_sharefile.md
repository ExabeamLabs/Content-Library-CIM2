Vendor: Citrix
==============
Product: Citrix ShareFile
-------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  67   |   26   |     6      |       3        |    3    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  app-activity<br> ↳[citrix-sharefile-sk4-app-activity-success-editnote](Ps/pC_citrixsharefilesk4appactivitysuccesseditnote.md)<br> ↳[citrix-sharefile-sk4-app-activity-success-usermodifiedpermission](Ps/pC_citrixsharefilesk4appactivitysuccessusermodifiedpermission.md)<br><br> app-login<br> ↳[citrix-sharefile-sk4-app-login-success-tfalogin](Ps/pC_citrixsharefilesk4apploginsuccesstfalogin.md)<br><br> failed-app-login<br> ↳[citrix-sharefile-sk4-app-login-fail-tfaloginfail](Ps/pC_citrixsharefilesk4apploginfailtfaloginfail.md)<br> ↳[citrix-sharefile-sk4-app-login-fail-loginlocked](Ps/pC_citrixsharefilesk4apploginfailloginlocked.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>15 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_citrix_citrix_sharefile_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  app-activity<br> ↳[citrix-sharefile-sk4-app-activity-success-editnote](Ps/pC_citrixsharefilesk4appactivitysuccesseditnote.md)<br> ↳[citrix-sharefile-sk4-app-activity-success-usermodifiedpermission](Ps/pC_citrixsharefilesk4appactivitysuccessusermodifiedpermission.md)<br><br> app-login<br> ↳[citrix-sharefile-sk4-app-login-success-tfalogin](Ps/pC_citrixsharefilesk4apploginsuccesstfalogin.md)<br><br> failed-app-login<br> ↳[citrix-sharefile-sk4-app-login-fail-tfaloginfail](Ps/pC_citrixsharefilesk4apploginfailtfaloginfail.md)<br> ↳[citrix-sharefile-sk4-app-login-fail-loginlocked](Ps/pC_citrixsharefilesk4apploginfailloginlocked.md)<br> | T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br> | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_citrix_citrix_sharefile_Account_Manipulation.md)    |
[Next Page -->>](2_ds_citrix_citrix_sharefile.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                                                                                                                                                                                                                 | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection                                                                                                                                                            | Command and Control                                                                                                                       | Exfiltration | Impact |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  | [Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |