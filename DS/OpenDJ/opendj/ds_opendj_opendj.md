Vendor: OpenDJ
==============
Product: OpenDJ
---------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  46   |   8    |     11     |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  authentication-successful<br> ↳[opendj-o-kv-endpoint-login-uid](Ps/pC_opendjokvendpointloginuid.md)<br> ↳[opendj-o-kv-endpoint-login-connectconn](Ps/pC_opendjokvendpointloginconnectconn.md)<br> ↳[opendj-o-kv-endpoint-login-msgid](Ps/pC_opendjokvendpointloginmsgid.md)<br><br> failed-logon<br> ↳[opendj-o-kv-endpoint-login-uid](Ps/pC_opendjokvendpointloginuid.md)<br> ↳[opendj-o-kv-endpoint-login-connectconn](Ps/pC_opendjokvendpointloginconnectconn.md)<br> ↳[opendj-o-kv-endpoint-login-msgid](Ps/pC_opendjokvendpointloginmsgid.md)<br> | T1078 - Valid Accounts<br>T1110 - Brute Force<br>T1133 - External Remote Services<br>    | [<ul><li>16 Rules</li></ul><ul><li>6 Models</li></ul>](RM/r_m_opendj_opendj_Abnormal_Authentication_&_Access.md) |
|    [Brute Force Attack](../../../UseCases/uc_brute_force_attack.md)    |  authentication-successful<br> ↳[opendj-o-kv-endpoint-login-uid](Ps/pC_opendjokvendpointloginuid.md)<br> ↳[opendj-o-kv-endpoint-login-connectconn](Ps/pC_opendjokvendpointloginconnectconn.md)<br> ↳[opendj-o-kv-endpoint-login-msgid](Ps/pC_opendjokvendpointloginmsgid.md)<br><br> failed-logon<br> ↳[opendj-o-kv-endpoint-login-uid](Ps/pC_opendjokvendpointloginuid.md)<br> ↳[opendj-o-kv-endpoint-login-connectconn](Ps/pC_opendjokvendpointloginconnectconn.md)<br> ↳[opendj-o-kv-endpoint-login-msgid](Ps/pC_opendjokvendpointloginmsgid.md)<br> | T1021.001 - Remote Services: Remote Desktop Protocol<br>T1110 - Brute Force<br>T1110.003 - T1110.003<br> | [<ul><li>9 Rules</li></ul>](RM/r_m_opendj_opendj_Brute_Force_Attack.md)    |
[Next Page -->>](2_ds_opendj_opendj.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                   | Execution | Persistence                                                                                                                                      | Privilege Escalation                                                                                                                                          | Defense Evasion                                                                                                                                                                                                                                                                                                                                                                           | Credential Access                                                                                                                                    | Discovery | Lateral Movement                                                                                                                                                                                                                                                                                                                                    | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550)<br><br>[Use Alternate Authentication Material: Pass the Hash](https://attack.mitre.org/techniques/T1550/002)<br><br>[Use Alternate Authentication Material: Pass the Ticket](https://attack.mitre.org/techniques/T1550/003)<br><br> | [Brute Force](https://attack.mitre.org/techniques/T1110)<br><br>[Steal or Forge Kerberos Tickets](https://attack.mitre.org/techniques/T1558)<br><br> |           | [Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210)<br><br>[Remote Services](https://attack.mitre.org/techniques/T1021)<br><br>[Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550)<br><br>[Remote Services: Remote Desktop Protocol](https://attack.mitre.org/techniques/T1021/001)<br><br> |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |