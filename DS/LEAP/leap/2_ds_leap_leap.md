|    Use-Case    | Activity Type (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  scheduled_task-trigger:success (app-activity)<br> ↳[leap-l-csv-app-activity-success-tuaccess](Ps/pC_leaplcsvappactivitysuccesstuaccess.md)<br> ↳[leap-l-str-app-activity-success-leapaccess](Ps/pC_leaplstrappactivitysuccessleapaccess.md)<br> ↳[leap-l-csv-app-activity-success-tuaudit](Ps/pC_leaplcsvappactivitysuccesstuaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaudit](Ps/pC_leaplcsvappactivitysuccessleapaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaccess](Ps/pC_leaplcsvappactivitysuccessleapaccess.md)<br> ↳[leap-l-str-app-activity-success-leapshk](Ps/pC_leaplstrappactivitysuccessleapshk.md)<br> ↳[leap-l-str-app-activity-success-leapaudit](Ps/pC_leaplstrappactivitysuccessleapaudit.md)<br><br> app-login:success (app-login)<br> ↳[leap-l-csv-app-activity-success-tuaccess](Ps/pC_leaplcsvappactivitysuccesstuaccess.md)<br> ↳[leap-l-str-app-activity-success-leapaccess](Ps/pC_leaplstrappactivitysuccessleapaccess.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>T1190 - Exploit Public Fasing Application<br>    | [<ul><li>42 Rules</li></ul><ul><li>24 Models</li></ul>](RM/r_m_leap_leap_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[leap-l-csv-app-activity-success-tuaccess](Ps/pC_leaplcsvappactivitysuccesstuaccess.md)<br> ↳[leap-l-str-app-activity-success-leapaccess](Ps/pC_leaplstrappactivitysuccessleapaccess.md)<br> ↳[leap-l-csv-app-activity-success-tuaudit](Ps/pC_leaplcsvappactivitysuccesstuaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaudit](Ps/pC_leaplcsvappactivitysuccessleapaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaccess](Ps/pC_leaplcsvappactivitysuccessleapaccess.md)<br> ↳[leap-l-str-app-activity-success-leapshk](Ps/pC_leaplstrappactivitysuccessleapshk.md)<br> ↳[leap-l-str-app-activity-success-leapaudit](Ps/pC_leaplstrappactivitysuccessleapaudit.md)<br><br> app-login:success (app-login)<br> ↳[leap-l-csv-app-activity-success-tuaccess](Ps/pC_leaplcsvappactivitysuccesstuaccess.md)<br> ↳[leap-l-str-app-activity-success-leapaccess](Ps/pC_leaplstrappactivitysuccessleapaccess.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>19 Rules</li></ul><ul><li>11 Models</li></ul>](RM/r_m_leap_leap_Data_Access.md)    |
|    [Data Leak](../../../UseCases/uc_data_leak.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[leap-l-csv-app-activity-success-tuaccess](Ps/pC_leaplcsvappactivitysuccesstuaccess.md)<br> ↳[leap-l-str-app-activity-success-leapaccess](Ps/pC_leaplstrappactivitysuccessleapaccess.md)<br> ↳[leap-l-csv-app-activity-success-tuaudit](Ps/pC_leaplcsvappactivitysuccesstuaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaudit](Ps/pC_leaplcsvappactivitysuccessleapaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaccess](Ps/pC_leaplcsvappactivitysuccessleapaccess.md)<br> ↳[leap-l-str-app-activity-success-leapshk](Ps/pC_leaplstrappactivitysuccessleapshk.md)<br> ↳[leap-l-str-app-activity-success-leapaudit](Ps/pC_leaplstrappactivitysuccessleapaudit.md)<br>    | T1114 - Email Collection<br>T1114.003 - Email Collection: Email Forwarding Rule<br>    | [<ul><li>3 Rules</li></ul>](RM/r_m_leap_leap_Data_Leak.md)    |
|         [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)         |  scheduled_task-trigger:success (app-activity)<br> ↳[leap-l-csv-app-activity-success-tuaccess](Ps/pC_leaplcsvappactivitysuccesstuaccess.md)<br> ↳[leap-l-str-app-activity-success-leapaccess](Ps/pC_leaplstrappactivitysuccessleapaccess.md)<br> ↳[leap-l-csv-app-activity-success-tuaudit](Ps/pC_leaplcsvappactivitysuccesstuaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaudit](Ps/pC_leaplcsvappactivitysuccessleapaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaccess](Ps/pC_leaplcsvappactivitysuccessleapaccess.md)<br> ↳[leap-l-str-app-activity-success-leapshk](Ps/pC_leaplstrappactivitysuccessleapshk.md)<br> ↳[leap-l-str-app-activity-success-leapaudit](Ps/pC_leaplstrappactivitysuccessleapaudit.md)<br><br> app-login:success (app-login)<br> ↳[leap-l-csv-app-activity-success-tuaccess](Ps/pC_leaplcsvappactivitysuccesstuaccess.md)<br> ↳[leap-l-str-app-activity-success-leapaccess](Ps/pC_leaplstrappactivitysuccessleapaccess.md)<br> | T1078 - Valid Accounts<br>T1098 - Account Manipulation<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br> | [<ul><li>6 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_leap_leap_Privilege_Abuse.md)    |
|    [Privilege Escalation](../../../UseCases/uc_privilege_escalation.md)    |  scheduled_task-trigger:success (app-activity)<br> ↳[leap-l-csv-app-activity-success-tuaccess](Ps/pC_leaplcsvappactivitysuccesstuaccess.md)<br> ↳[leap-l-str-app-activity-success-leapaccess](Ps/pC_leaplstrappactivitysuccessleapaccess.md)<br> ↳[leap-l-csv-app-activity-success-tuaudit](Ps/pC_leaplcsvappactivitysuccesstuaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaudit](Ps/pC_leaplcsvappactivitysuccessleapaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaccess](Ps/pC_leaplcsvappactivitysuccessleapaccess.md)<br> ↳[leap-l-str-app-activity-success-leapshk](Ps/pC_leaplstrappactivitysuccessleapshk.md)<br> ↳[leap-l-str-app-activity-success-leapaudit](Ps/pC_leaplstrappactivitysuccessleapaudit.md)<br>    | T1098 - Account Manipulation<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>    | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_leap_leap_Privilege_Escalation.md)      |
|     [Privileged Activity](../../../UseCases/uc_privileged_activity.md)     |  scheduled_task-trigger:success (app-activity)<br> ↳[leap-l-csv-app-activity-success-tuaccess](Ps/pC_leaplcsvappactivitysuccesstuaccess.md)<br> ↳[leap-l-str-app-activity-success-leapaccess](Ps/pC_leaplstrappactivitysuccessleapaccess.md)<br> ↳[leap-l-csv-app-activity-success-tuaudit](Ps/pC_leaplcsvappactivitysuccesstuaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaudit](Ps/pC_leaplcsvappactivitysuccessleapaudit.md)<br> ↳[leap-l-csv-app-activity-success-leapaccess](Ps/pC_leaplcsvappactivitysuccessleapaccess.md)<br> ↳[leap-l-str-app-activity-success-leapshk](Ps/pC_leaplstrappactivitysuccessleapshk.md)<br> ↳[leap-l-str-app-activity-success-leapaudit](Ps/pC_leaplstrappactivitysuccessleapaudit.md)<br><br> app-login:success (app-login)<br> ↳[leap-l-csv-app-activity-success-tuaccess](Ps/pC_leaplcsvappactivitysuccesstuaccess.md)<br> ↳[leap-l-str-app-activity-success-leapaccess](Ps/pC_leaplstrappactivitysuccessleapaccess.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_leap_leap_Privileged_Activity.md)       |