Vendor: Google
==============
Product: Workspace
------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  99   |   43   |     7      |       6        |    6    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  app-activity<br> ↳[google-workspace-sk4-app-success-activity](Ps/pC_googleworkspacesk4appsuccessactivity.md)<br> ↳[google-workspace-sk4-app-success-token](Ps/pC_googleworkspacesk4appsuccesstoken.md)<br> ↳[google-workspace-sk4-app-activity-success-groups](Ps/pC_googleworkspacesk4appactivitysuccessgroups.md)<br> ↳[google-workspace-sk4-app-activity-success-admin](Ps/pC_googleworkspacesk4appactivitysuccessadmin.md)<br> ↳[google-workspace-json-app-activity-success-calendar](Ps/pC_googleworkspacejsonappactivitysuccesscalendar.md)<br> ↳[google-workspace-sk4-app-activity-success-mobile](Ps/pC_googleworkspacesk4appactivitysuccessmobile.md)<br> ↳[google-workspace-sk4-app-activity-success-calendar](Ps/pC_googleworkspacesk4appactivitysuccesscalendar.md)<br><br> app-login<br> ↳[google-workspace-sk4-app-success-activity](Ps/pC_googleworkspacesk4appsuccessactivity.md)<br> ↳[google-workspace-sk4-app-success-token](Ps/pC_googleworkspacesk4appsuccesstoken.md)<br> ↳[google-workspace-sk4-app-login-success-googleapps2](Ps/pC_googleworkspacesk4apploginsuccessgoogleapps2.md)<br> ↳[google-workspace-json-app-login-success-authorize](Ps/pC_googleworkspacejsonapploginsuccessauthorize.md)<br><br> dlp-email-alert-in<br> ↳[google-workspace-cef-email-receive](Ps/pC_googleworkspacecefemailreceive.md)<br><br> dlp-email-alert-in-failed<br> ↳[google-workspace-cef-email-receive](Ps/pC_googleworkspacecefemailreceive.md)<br><br> dlp-email-alert-out<br> ↳[google-workspace-cef-email-send](Ps/pC_googleworkspacecefemailsend.md)<br><br> dlp-email-alert-out-failed<br> ↳[google-workspace-cef-email-send](Ps/pC_googleworkspacecefemailsend.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>12 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_google_workspace_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  app-activity<br> ↳[google-workspace-sk4-app-success-activity](Ps/pC_googleworkspacesk4appsuccessactivity.md)<br> ↳[google-workspace-sk4-app-success-token](Ps/pC_googleworkspacesk4appsuccesstoken.md)<br> ↳[google-workspace-sk4-app-activity-success-groups](Ps/pC_googleworkspacesk4appactivitysuccessgroups.md)<br> ↳[google-workspace-sk4-app-activity-success-admin](Ps/pC_googleworkspacesk4appactivitysuccessadmin.md)<br> ↳[google-workspace-json-app-activity-success-calendar](Ps/pC_googleworkspacejsonappactivitysuccesscalendar.md)<br> ↳[google-workspace-sk4-app-activity-success-mobile](Ps/pC_googleworkspacesk4appactivitysuccessmobile.md)<br> ↳[google-workspace-sk4-app-activity-success-calendar](Ps/pC_googleworkspacesk4appactivitysuccesscalendar.md)<br><br> app-login<br> ↳[google-workspace-sk4-app-success-activity](Ps/pC_googleworkspacesk4appsuccessactivity.md)<br> ↳[google-workspace-sk4-app-success-token](Ps/pC_googleworkspacesk4appsuccesstoken.md)<br> ↳[google-workspace-sk4-app-login-success-googleapps2](Ps/pC_googleworkspacesk4apploginsuccessgoogleapps2.md)<br> ↳[google-workspace-json-app-login-success-authorize](Ps/pC_googleworkspacejsonapploginsuccessauthorize.md)<br><br> dlp-email-alert-in<br> ↳[google-workspace-cef-email-receive](Ps/pC_googleworkspacecefemailreceive.md)<br><br> dlp-email-alert-in-failed<br> ↳[google-workspace-cef-email-receive](Ps/pC_googleworkspacecefemailreceive.md)<br><br> dlp-email-alert-out<br> ↳[google-workspace-cef-email-send](Ps/pC_googleworkspacecefemailsend.md)<br><br> dlp-email-alert-out-failed<br> ↳[google-workspace-cef-email-send](Ps/pC_googleworkspacecefemailsend.md)<br> | T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br> | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_google_workspace_Account_Manipulation.md)    |
[Next Page -->>](2_ds_google_workspace.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                                                                                                                                                                                                                 | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection                                                                                                                                                            | Command and Control                                                                                                                       | Exfiltration                                                                                                                                                                                                                                         | Impact |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  | [Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> | [Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048)<br><br>[Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol](https://attack.mitre.org/techniques/T1048/003)<br><br> |        |