Vendor: CA Technologies
=======================
Product: CA Privileged Access Manager Server Control
----------------------------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  103  |   37   |     16     |       7        |    7    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  ""app-logout:success""<br> ↳[ca-pamsc-kv-app-logout-success-conntimedout](Ps/pC_capamsckvapplogoutsuccessconntimedout.md)<br> ↳[ca-pamsc-kv-app-logout-success-connclosed](Ps/pC_capamsckvapplogoutsuccessconnclosed.md)<br> ↳[ca-pamsc-kv-app-logout-success-logout](Ps/pC_capamsckvapplogoutsuccesslogout.md)<br> ↳[ca-pamsc-kv-app-logout-success-connterminated](Ps/pC_capamsckvapplogoutsuccessconnterminated.md)<br><br> ""user-password-read:success""<br> ↳[ca-pamsc-xml-user-password-read-commandinitiator](Ps/pC_capamscxmluserpasswordreadcommandinitiator.md)<br><br> account-switch<br> ↳[ca-pamsc-kv-user-switch-success-0016](Ps/pC_capamsckvuserswitchsuccess0016.md)<br> ↳[ca-pamsc-kv-user-switch-success-0023](Ps/pC_capamsckvuserswitchsuccess0023.md)<br><br> app-activity<br> ↳[ca-pamsc-kv-app-activity-sessionrecording](Ps/pC_capamsckvappactivitysessionrecording.md)<br><br> app-login<br> ↳[ca-pamsc-kv-app-login-success-sso](Ps/pC_capamsckvapploginsuccesssso.md)<br><br> authentication-successful<br> ↳[ca-pamsc-csv-endpoint-login-success-loggedin](Ps/pC_capamsccsvendpointloginsuccessloggedin.md)<br><br> failed-logon<br> ↳[ca-pamsc-csv-endpoint-login-fail-baduserid](Ps/pC_capamsccsvendpointloginfailbaduserid.md)<br> ↳[ca-pamsc-csv-endpoint-login-fail-ldap](Ps/pC_capamsccsvendpointloginfailldap.md)<br> | T1078 - Valid Accounts<br>T1110 - Brute Force<br>T1133 - External Remote Services<br> | [<ul><li>17 Rules</li></ul><ul><li>6 Models</li></ul>](RM/r_m_ca_technologies_ca_privileged_access_manager_server_control_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  ""app-logout:success""<br> ↳[ca-pamsc-kv-app-logout-success-conntimedout](Ps/pC_capamsckvapplogoutsuccessconntimedout.md)<br> ↳[ca-pamsc-kv-app-logout-success-connclosed](Ps/pC_capamsckvapplogoutsuccessconnclosed.md)<br> ↳[ca-pamsc-kv-app-logout-success-logout](Ps/pC_capamsckvapplogoutsuccesslogout.md)<br> ↳[ca-pamsc-kv-app-logout-success-connterminated](Ps/pC_capamsckvapplogoutsuccessconnterminated.md)<br><br> ""user-password-read:success""<br> ↳[ca-pamsc-xml-user-password-read-commandinitiator](Ps/pC_capamscxmluserpasswordreadcommandinitiator.md)<br><br> account-switch<br> ↳[ca-pamsc-kv-user-switch-success-0016](Ps/pC_capamsckvuserswitchsuccess0016.md)<br> ↳[ca-pamsc-kv-user-switch-success-0023](Ps/pC_capamsckvuserswitchsuccess0023.md)<br><br> app-activity<br> ↳[ca-pamsc-kv-app-activity-sessionrecording](Ps/pC_capamsckvappactivitysessionrecording.md)<br><br> app-login<br> ↳[ca-pamsc-kv-app-login-success-sso](Ps/pC_capamsckvapploginsuccesssso.md)<br><br> authentication-successful<br> ↳[ca-pamsc-csv-endpoint-login-success-loggedin](Ps/pC_capamsccsvendpointloginsuccessloggedin.md)<br><br> failed-logon<br> ↳[ca-pamsc-csv-endpoint-login-fail-baduserid](Ps/pC_capamsccsvendpointloginfailbaduserid.md)<br> ↳[ca-pamsc-csv-endpoint-login-fail-ldap](Ps/pC_capamsccsvendpointloginfailldap.md)<br> | T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>    | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_ca_technologies_ca_privileged_access_manager_server_control_Account_Manipulation.md)    |
[Next Page -->>](2_ds_ca_technologies_ca_privileged_access_manager_server_control.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                                                                                                                                                                                                                 | Privilege Escalation                                                                                                                                          | Defense Evasion                                                                                                                                                                                                                                                                                                                                                                           | Credential Access                                                                                                                                                                                                                         | Discovery | Lateral Movement                                                                                                                                                                                                                                                                                                                                    | Collection                                                                                                                                                            | Command and Control                                                                                                                       | Exfiltration | Impact |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Account Manipulation: Exchange Email Delegate Permissions](https://attack.mitre.org/techniques/T1098/002)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550)<br><br>[Use Alternate Authentication Material: Pass the Hash](https://attack.mitre.org/techniques/T1550/002)<br><br>[Use Alternate Authentication Material: Pass the Ticket](https://attack.mitre.org/techniques/T1550/003)<br><br> | [Brute Force](https://attack.mitre.org/techniques/T1110)<br><br>[Steal or Forge Kerberos Tickets](https://attack.mitre.org/techniques/T1558)<br><br>[Credentials from Password Stores](https://attack.mitre.org/techniques/T1555)<br><br> |           | [Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210)<br><br>[Remote Services](https://attack.mitre.org/techniques/T1021)<br><br>[Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550)<br><br>[Remote Services: Remote Desktop Protocol](https://attack.mitre.org/techniques/T1021/001)<br><br> | [Email Collection](https://attack.mitre.org/techniques/T1114)<br><br>[Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003)<br><br> | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |