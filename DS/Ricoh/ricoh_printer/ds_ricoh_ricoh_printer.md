Vendor: Ricoh
=============
Product: Ricoh Printer
----------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   2    |         2          |       1        |    1    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  printer-activity:success (print-activity)<br> ↳[ricoh-r-kv-printer-activity-success-3](Ps/pC_ricohrkvprinteractivitysuccess3.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_ricoh_ricoh_printer_Abnormal_Authentication_&_Access.md)    |
|    [Data Leak](../../../UseCases/uc_data_leak.md)    |  printer-activity:success (print-activity)<br> ↳[ricoh-r-kv-printer-activity-success-3](Ps/pC_ricohrkvprinteractivitysuccess3.md)<br> | T1052 - Exfiltration Over Physical Medium<br> | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_ricoh_ricoh_printer_Data_Leak.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration                                                                           | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | -------------------------------------------------------------------------------------- | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     | [Exfiltration Over Physical Medium](https://attack.mitre.org/techniques/T1052)<br><br> |        |