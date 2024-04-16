Vendor: Buildkite
=================
Product: Buildkite
------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  35   |   19   |         4          |       1        |    4    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  dlp-alert<br> ↳[buildkite-bk-json-app-notification-success-api](Ps/pC_buildkitebkjsonappnotificationsuccessapi.md)<br> ↳[buildkite-bk-json-app-notification-success-schedule](Ps/pC_buildkitebkjsonappnotificationsuccessschedule.md)<br> ↳[buildkite-bk-json-app-notification-success-ui](Ps/pC_buildkitebkjsonappnotificationsuccessui.md)<br> ↳[buildkite-bk-json-app-notification-success-triggerjob](Ps/pC_buildkitebkjsonappnotificationsuccesstriggerjob.md)<br> ↳[buildkite-bk-json-app-notification-success-webhook](Ps/pC_buildkitebkjsonappnotificationsuccesswebhook.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>31 Rules</li></ul><ul><li>17 Models</li></ul>](RM/r_m_buildkite_buildkite_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  dlp-alert<br> ↳[buildkite-bk-json-app-notification-success-api](Ps/pC_buildkitebkjsonappnotificationsuccessapi.md)<br> ↳[buildkite-bk-json-app-notification-success-schedule](Ps/pC_buildkitebkjsonappnotificationsuccessschedule.md)<br> ↳[buildkite-bk-json-app-notification-success-ui](Ps/pC_buildkitebkjsonappnotificationsuccessui.md)<br> ↳[buildkite-bk-json-app-notification-success-triggerjob](Ps/pC_buildkitebkjsonappnotificationsuccesstriggerjob.md)<br> ↳[buildkite-bk-json-app-notification-success-webhook](Ps/pC_buildkitebkjsonappnotificationsuccesswebhook.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>31 Rules</li></ul><ul><li>17 Models</li></ul>](RM/r_m_buildkite_buildkite_Data_Leak.md)         |
[Next Page -->>](2_ds_buildkite_buildkite.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |