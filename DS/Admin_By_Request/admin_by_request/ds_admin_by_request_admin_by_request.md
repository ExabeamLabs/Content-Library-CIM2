Vendor: Admin By Request
========================
Product: Admin By Request
-------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  20   |   15   |         2          |       2        |    2    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP          | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  user-privilege-assign:success (privileged-access)<br> ↳[adminbyrequest-a-json-user-privilege-use-success-adminsession](Ps/pC_adminbyrequestajsonuserprivilegeusesuccessadminsession.md)<br><br> user-privilege-use:success (privileged-object-access)<br> ↳[adminbyrequest-a-json-user-privilege-use-success-runasadmin](Ps/pC_adminbyrequestajsonuserprivilegeusesuccessrunasadmin.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_admin_by_request_admin_by_request_Abnormal_Authentication_&_Access.md) |
|    [Malware](../../../UseCases/uc_malware.md)    |  user-privilege-assign:success (privileged-access)<br> ↳[adminbyrequest-a-json-user-privilege-use-success-adminsession](Ps/pC_adminbyrequestajsonuserprivilegeusesuccessadminsession.md)<br><br> user-privilege-use:success (privileged-object-access)<br> ↳[adminbyrequest-a-json-user-privilege-use-success-runasadmin](Ps/pC_adminbyrequestajsonuserprivilegeusesuccessrunasadmin.md)<br> | TA0002 - TA0002<br>        | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_admin_by_request_admin_by_request_Malware.md)    |
|    [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)    |  user-privilege-assign:success (privileged-access)<br> ↳[adminbyrequest-a-json-user-privilege-use-success-adminsession](Ps/pC_adminbyrequestajsonuserprivilegeusesuccessadminsession.md)<br>    | T1078 - Valid Accounts<br> | [<ul><li>5 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_admin_by_request_admin_by_request_Privilege_Abuse.md)    |
|    [Privileged Activity](../../../UseCases/uc_privileged_activity.md)    |  user-privilege-assign:success (privileged-access)<br> ↳[adminbyrequest-a-json-user-privilege-use-success-adminsession](Ps/pC_adminbyrequestajsonuserprivilegeusesuccessadminsession.md)<br>    | TA0002 - TA0002<br>        | [<ul><li>10 Rules</li></ul><ul><li>7 Models</li></ul>](RM/r_m_admin_by_request_admin_by_request_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |