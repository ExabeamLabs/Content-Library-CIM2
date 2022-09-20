Vendor: Zoom
============
Product: Zoom
-------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   1    |     1      |       5        |    5    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Workforce Protection](../../../UseCases/uc_workforce_protection.md) |  web-meeting-created<br> ↳[zoom-z-meeting-create-success-created](Ps/pC_zoomzmeetingcreatesuccesscreated.md)<br><br> web-meeting-ended<br> ↳[zoom-z-meeting-end-success-ended](Ps/pC_zoomzmeetingendsuccessended.md)<br><br> web-meeting-participant-joined<br> ↳[zoom-z-meeting-member-join-success-participant](Ps/pC_zoomzmeetingmemberjoinsuccessparticipant.md)<br><br> web-meeting-started<br> ↳[zoom-z-meeting-start-success-started](Ps/pC_zoomzmeetingstartsuccessstarted.md)<br><br> web-meeting-updated<br> ↳[zoom-z-meeting-modify-success-updated](Ps/pC_zoomzmeetingmodifysuccessupdated.md)<br> | T1078.004 - Valid Accounts: Cloud Accounts<br> | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_zoom_zoom_Workforce_Protection.md) |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                             | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Valid Accounts: Cloud Accounts](https://attack.mitre.org/techniques/T1078/004)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |