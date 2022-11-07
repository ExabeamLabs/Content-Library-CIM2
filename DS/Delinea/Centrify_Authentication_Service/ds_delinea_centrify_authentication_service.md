Vendor: Delinea
===============
Product: Centrify Authentication Service
----------------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  18   |   5    |     3      |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  authentication-successful<br> ↳[delinea-centrifyas-kv-app-authentication-success-54203](Ps/pC_delineacentrifyaskvappauthenticationsuccess54203.md)<br> ↳[delinea-centrifyas-kv-app-authentication-success-54202](Ps/pC_delineacentrifyaskvappauthenticationsuccess54202.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br> | [<ul><li>11 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_delinea_centrify_authentication_service_Abnormal_Authentication_&_Access.md) |
|          [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md)          |  authentication-successful<br> ↳[delinea-centrifyas-kv-app-authentication-success-54203](Ps/pC_delineacentrifyaskvappauthenticationsuccess54203.md)<br> ↳[delinea-centrifyas-kv-app-authentication-success-54202](Ps/pC_delineacentrifyaskvappauthenticationsuccess54202.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br> | [<ul><li>7 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_delinea_centrify_authentication_service_Compromised_Credentials.md)    |
|    [Lateral Movement](../../../UseCases/uc_lateral_movement.md)    |  authentication-successful<br> ↳[delinea-centrifyas-kv-app-authentication-success-54203](Ps/pC_delineacentrifyaskvappauthenticationsuccess54203.md)<br> ↳[delinea-centrifyas-kv-app-authentication-success-54202](Ps/pC_delineacentrifyaskvappauthenticationsuccess54202.md)<br> | T1090.003 - Proxy: Multi-hop Proxy<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_delinea_centrify_authentication_service_Lateral_Movement.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  authentication-successful<br> ↳[delinea-centrifyas-kv-app-authentication-success-54203](Ps/pC_delineacentrifyaskvappauthenticationsuccess54203.md)<br> ↳[delinea-centrifyas-kv-app-authentication-success-54202](Ps/pC_delineacentrifyaskvappauthenticationsuccess54202.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_delinea_centrify_authentication_service_Malware.md)    |
|    [Ransomware](../../../UseCases/uc_ransomware.md)    |  authentication-successful<br> ↳[delinea-centrifyas-kv-app-authentication-success-54203](Ps/pC_delineacentrifyaskvappauthenticationsuccess54203.md)<br> ↳[delinea-centrifyas-kv-app-authentication-success-54202](Ps/pC_delineacentrifyaskvappauthenticationsuccess54202.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_delinea_centrify_authentication_service_Ransomware.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                   | Execution | Persistence                                                                                                                                      | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |