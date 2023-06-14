Vendor: Amazon
==============
Product: AWS GuardDuty
----------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  43   |   25   |         5          |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-login<br> ↳[amazon-awsguardduty-json-database-login-success-rdssuccessfullogin](Ps/pC_amazonawsguarddutyjsondatabaseloginsuccessrdssuccessfullogin.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_amazon_aws_guardduty_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-login<br> ↳[amazon-awsguardduty-json-database-login-success-rdssuccessfullogin](Ps/pC_amazonawsguarddutyjsondatabaseloginsuccessrdssuccessfullogin.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_amazon_aws_guardduty_Data_Access.md)    |
[Next Page -->>](2_ds_amazon_aws_guardduty.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |