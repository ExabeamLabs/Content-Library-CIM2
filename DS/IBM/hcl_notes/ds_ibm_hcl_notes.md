Vendor: IBM
===========
Product: HCL Notes
------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   0    |         1          |       2        |    2    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP          | Content    |
|:----:| ---- | ---- | ---- |
|     [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)     |  file-download:success (file-download)<br> ↳[ibm-hclnotes-str-file-download-success-pulling](Ps/pC_ibmhclnotesstrfiledownloadsuccesspulling.md)<br><br> file-upload:success (file-upload)<br> ↳[ibm-hclnotes-str-file-upload-success-pushing](Ps/pC_ibmhclnotesstrfileuploadsuccesspushing.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_ibm_hcl_notes_Privilege_Abuse.md)     |
| [Privileged Activity](../../../UseCases/uc_privileged_activity.md) |  file-download:success (file-download)<br> ↳[ibm-hclnotes-str-file-download-success-pulling](Ps/pC_ibmhclnotesstrfiledownloadsuccesspulling.md)<br><br> file-upload:success (file-upload)<br> ↳[ibm-hclnotes-str-file-upload-success-pushing](Ps/pC_ibmhclnotesstrfileuploadsuccesspushing.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_ibm_hcl_notes_Privileged_Activity.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |