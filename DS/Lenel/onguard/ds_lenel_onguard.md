Vendor: Lenel
=============
Product: OnGuard
----------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  12   |   6    |         1          |       1        |    3    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP          | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  physical_location-access:fail (failed-physical-access)<br> ↳[lenel-og-kv-physical-location-access-evdescr](Ps/pC_lenelogkvphysicallocationaccessevdescr.md)<br> ↳[lenel-og-kv-physical-location-access-accessgranted-1](Ps/pC_lenelogkvphysicallocationaccessaccessgranted1.md)<br><br> physical_location-access:success (physical-access)<br> ↳[lenel-og-kv-physical-location-access-evdescr](Ps/pC_lenelogkvphysicallocationaccessevdescr.md)<br> ↳[lenel-og-kv-physical-location-access-accessgranted-1](Ps/pC_lenelogkvphysicallocationaccessaccessgranted1.md)<br> ↳[lenel-og-json-physical-location-access-success-panelname](Ps/pC_lenelogjsonphysicallocationaccesssuccesspanelname.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>3 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_lenel_onguard_Abnormal_Authentication_&_Access.md) |
|    [Physical Security](../../../UseCases/uc_physical_security.md)    |  physical_location-access:fail (failed-physical-access)<br> ↳[lenel-og-kv-physical-location-access-evdescr](Ps/pC_lenelogkvphysicallocationaccessevdescr.md)<br> ↳[lenel-og-kv-physical-location-access-accessgranted-1](Ps/pC_lenelogkvphysicallocationaccessaccessgranted1.md)<br><br> physical_location-access:success (physical-access)<br> ↳[lenel-og-kv-physical-location-access-evdescr](Ps/pC_lenelogkvphysicallocationaccessevdescr.md)<br> ↳[lenel-og-kv-physical-location-access-accessgranted-1](Ps/pC_lenelogkvphysicallocationaccessaccessgranted1.md)<br> ↳[lenel-og-json-physical-location-access-success-panelname](Ps/pC_lenelogjsonphysicallocationaccesssuccesspanelname.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>9 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_lenel_onguard_Physical_Security.md)    |
[Next Page -->>](2_ds_lenel_onguard.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |