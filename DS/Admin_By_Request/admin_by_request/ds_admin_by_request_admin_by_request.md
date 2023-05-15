Vendor: Admin By Request
========================
Product: Admin By Request
-------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   3    |         2          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP          | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  privileged-object-access<br> ↳[adminbyrequest-a-json-user-privilege-use-success-adminsession](Ps/pC_adminbyrequestajsonuserprivilegeusesuccessadminsession.md)<br> ↳[adminbyrequest-a-json-user-privilege-use-success-runasadmin](Ps/pC_adminbyrequestajsonuserprivilegeusesuccessrunasadmin.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_admin_by_request_admin_by_request_Abnormal_Authentication_&_Access.md) |
|    [Malware](../../../UseCases/uc_malware.md)    |  privileged-object-access<br> ↳[adminbyrequest-a-json-user-privilege-use-success-adminsession](Ps/pC_adminbyrequestajsonuserprivilegeusesuccessadminsession.md)<br> ↳[adminbyrequest-a-json-user-privilege-use-success-runasadmin](Ps/pC_adminbyrequestajsonuserprivilegeusesuccessrunasadmin.md)<br> | TA0002 - TA0002<br>        | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_admin_by_request_admin_by_request_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |