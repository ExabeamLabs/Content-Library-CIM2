Vendor: Symantec
================
Product: Symantec Critical System Protection
--------------------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  69   |   23   |     14     |       4        |    4    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  account-switch<br> ↳[symantec-csp-kv-user-switch-success-successfulsu](Ps/pC_symanteccspkvuserswitchsuccesssuccessfulsu.md)<br><br> config-change<br> ↳[symantec-csp-kv-configuration-modify-success-groupmembershipchanged](Ps/pC_symanteccspkvconfigurationmodifysuccessgroupmembershipchanged.md)<br> ↳[symantec-csp-kv-configuration-modify-success-primarygroupchanged](Ps/pC_symanteccspkvconfigurationmodifysuccessprimarygroupchanged.md)<br><br> failed-logon<br> ↳[symantec-csp-json-endpoint-login-fail-failedsuto](Ps/pC_symanteccspjsonendpointloginfailfailedsuto.md)<br><br> member-added<br> ↳[symantec-csp-kv-group-member-add-success-groupcreated](Ps/pC_symanteccspkvgroupmemberaddsuccessgroupcreated.md)<br> | T1078 - Valid Accounts<br>T1110 - Brute Force<br>          | [<ul><li>8 Rules</li></ul><ul><li>3 Models</li></ul>](RM/r_m_symantec_symantec_critical_system_protection_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  account-switch<br> ↳[symantec-csp-kv-user-switch-success-successfulsu](Ps/pC_symanteccspkvuserswitchsuccesssuccessfulsu.md)<br><br> config-change<br> ↳[symantec-csp-kv-configuration-modify-success-groupmembershipchanged](Ps/pC_symanteccspkvconfigurationmodifysuccessgroupmembershipchanged.md)<br> ↳[symantec-csp-kv-configuration-modify-success-primarygroupchanged](Ps/pC_symanteccspkvconfigurationmodifysuccessprimarygroupchanged.md)<br><br> failed-logon<br> ↳[symantec-csp-json-endpoint-login-fail-failedsuto](Ps/pC_symanteccspjsonendpointloginfailfailedsuto.md)<br><br> member-added<br> ↳[symantec-csp-kv-group-member-add-success-groupcreated](Ps/pC_symanteccspkvgroupmemberaddsuccessgroupcreated.md)<br> | T1098 - Account Manipulation<br>T1136 - Create Account<br> | [<ul><li>24 Rules</li></ul><ul><li>12 Models</li></ul>](RM/r_m_symantec_symantec_critical_system_protection_Account_Manipulation.md)    |
[Next Page -->>](2_ds_symantec_symantec_critical_system_protection.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                      | Execution | Persistence                                                                                                                                                                                                     | Privilege Escalation                                                                                                                                          | Defense Evasion                                                                                                                                                                                                                                                                                                                                                                           | Credential Access                                                                                                                                                                                                                         | Discovery | Lateral Movement                                                                                                                                                                                                                                                                                                                                    | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Create Account](https://attack.mitre.org/techniques/T1136)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550)<br><br>[Use Alternate Authentication Material: Pass the Hash](https://attack.mitre.org/techniques/T1550/002)<br><br>[Use Alternate Authentication Material: Pass the Ticket](https://attack.mitre.org/techniques/T1550/003)<br><br> | [Brute Force](https://attack.mitre.org/techniques/T1110)<br><br>[Steal or Forge Kerberos Tickets](https://attack.mitre.org/techniques/T1558)<br><br>[Credentials from Password Stores](https://attack.mitre.org/techniques/T1555)<br><br> |           | [Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210)<br><br>[Remote Services](https://attack.mitre.org/techniques/T1021)<br><br>[Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550)<br><br>[Remote Services: Remote Desktop Protocol](https://attack.mitre.org/techniques/T1021/001)<br><br> |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |