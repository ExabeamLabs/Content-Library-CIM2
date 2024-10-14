Vendor: Microsoft
=================
Product: Active Directory Federation Services
---------------------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         1          |       1        |    0    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP       | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  user-lock:success (account-lockout)<br> ↳[microsoft-evsecurity-cef-user-lock-success-516](Ps/pC_microsoftevsecuritycefuserlocksuccess516.md)<br> | T1110 - Brute Force<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_active_directory_federation_services_Abnormal_Authentication_&_Access.md) |
|    [Brute Force Attack](../../../UseCases/uc_brute_force_attack.md)    |  user-lock:success (account-lockout)<br> ↳[microsoft-evsecurity-cef-user-lock-success-516](Ps/pC_microsoftevsecuritycefuserlocksuccess516.md)<br> | T1110 - Brute Force<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_active_directory_federation_services_Brute_Force_Attack.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access                                                | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ---------------------------------------------------------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 | [Brute Force](https://attack.mitre.org/techniques/T1110)<br><br> |           |                  |            |                     |              |        |