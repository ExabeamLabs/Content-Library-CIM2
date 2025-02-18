Vendor: Specops
===============
Product: Specops Password
-------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   1    |         2          |       2        |    2    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  user-password-reset:success (account-password-reset)<br> ↳[specops-spr-xml-user-password-reset-success-passwordresetsucceeded](Ps/pC_specopssprxmluserpasswordresetsuccesspasswordresetsucceeded.md)<br><br> user-unlock:success (account-unlocked)<br> ↳[specops-spr-xml-user-unlock-success-unlock](Ps/pC_specopssprxmluserunlocksuccessunlock.md)<br> | T1078 - Valid Accounts<br>       | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_specops_specops_password_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  user-password-reset:success (account-password-reset)<br> ↳[specops-spr-xml-user-password-reset-success-passwordresetsucceeded](Ps/pC_specopssprxmluserpasswordresetsuccesspasswordresetsucceeded.md)<br>    | T1098 - Account Manipulation<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_specops_specops_password_Account_Manipulation.md)    |
|    [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)    |  user-password-reset:success (account-password-reset)<br> ↳[specops-spr-xml-user-password-reset-success-passwordresetsucceeded](Ps/pC_specopssprxmluserpasswordresetsuccesspasswordresetsucceeded.md)<br>    | T1098 - Account Manipulation<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_specops_specops_password_Privilege_Abuse.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                                                                                                  | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |