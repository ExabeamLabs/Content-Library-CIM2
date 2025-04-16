Vendor: HP
==========
Product: ArubaOS
----------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  13   |   6    |         3          |       2        |    5    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  endpoint-login:success (nac-logon)<br> ↳[hp-arubaos-str-endpoint-login-success-5209](Ps/pC_hparubaosstrendpointloginsuccess5209.md)<br> ↳[hp-arubaos-str-endpoint-login-success-00179](Ps/pC_hparubaosstrendpointloginsuccess00179.md)<br> ↳[hp-arubaos-str-endpoint-login-success-03362](Ps/pC_hparubaosstrendpointloginsuccess03362.md)<br> | T1021 - Remote Services<br>T1078 - Valid Accounts<br> | [<ul><li>8 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_hp_arubaos_Abnormal_Authentication_&_Access.md) |
|          [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md)          |  endpoint-login:success (nac-logon)<br> ↳[hp-arubaos-str-endpoint-login-success-5209](Ps/pC_hparubaosstrendpointloginsuccess5209.md)<br> ↳[hp-arubaos-str-endpoint-login-success-00179](Ps/pC_hparubaosstrendpointloginsuccess00179.md)<br> ↳[hp-arubaos-str-endpoint-login-success-03362](Ps/pC_hparubaosstrendpointloginsuccess03362.md)<br> | T1021 - Remote Services<br>T1078 - Valid Accounts<br> | [<ul><li>6 Rules</li></ul><ul><li>3 Models</li></ul>](RM/r_m_hp_arubaos_Compromised_Credentials.md)          |
[Next Page -->>](2_ds_hp_arubaos.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement                                                                                                                                         | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           | [Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210)<br><br>[Remote Services](https://attack.mitre.org/techniques/T1021)<br><br> |            |                     |              |        |