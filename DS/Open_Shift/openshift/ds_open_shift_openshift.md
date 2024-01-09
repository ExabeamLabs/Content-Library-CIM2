Vendor: Open Shift
==================
Product: OpenShift
------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   8   |   3    |         6          |       1        |    0    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Evasion](../../../UseCases/uc_evasion.md) |  registry-write<br> ↳[openshift-o-kv-app-activity-annotations](Ps/pC_openshiftokvappactivityannotations.md)<br> | T1564.001 - T1564.001<br>T1564.002 - T1564.002<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_open_shift_openshift_Evasion.md)    |
| [Malware](../../../UseCases/uc_malware.md) |  registry-write<br> ↳[openshift-o-kv-app-activity-annotations](Ps/pC_openshiftokvappactivityannotations.md)<br> | T1112 - Modify Registry<br>T1547.001 - T1547.001<br>T1574.010 - T1574.010<br>T1574.011 - T1574.011<br> | [<ul><li>6 Rules</li></ul><ul><li>3 Models</li></ul>](RM/r_m_open_shift_openshift_Malware.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence                                                                                                                                                      | Privilege Escalation                                                                                                                                             | Defense Evasion                                                                                                                                                                                                   | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
|                |           | [Hijack Execution Flow](https://attack.mitre.org/techniques/T1574)<br><br>[Boot or Logon Autostart Execution](https://attack.mitre.org/techniques/T1547)<br><br> | [Hijack Execution Flow](https://attack.mitre.org/techniques/T1574)<br><br>[Boot or Logon Autostart Execution](https://attack.mitre.org/techniques/T1547)<br><br> | [Hide Artifacts](https://attack.mitre.org/techniques/T1564)<br><br>[Modify Registry](https://attack.mitre.org/techniques/T1112)<br><br>[Hijack Execution Flow](https://attack.mitre.org/techniques/T1574)<br><br> |                   |           |                  |            |                     |              |        |