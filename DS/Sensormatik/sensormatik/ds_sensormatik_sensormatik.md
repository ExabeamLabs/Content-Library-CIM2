Vendor: Sensormatik
===================
Product: Sensormatik
--------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  12   |   6    |         1          |       1        |    1    |

|    Use-Case    | Activity Types(Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP          | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  physical_location-access:fail(failed-physical-access)<br> ↳[sensormatik-s-cef-physical-location-access-success-sensormatik](Ps/pC_sensormatikscefphysicallocationaccesssuccesssensormatik.md)<br> ↳[sensormatik-s-kv-physical-location-access-cardadmitted](Ps/pC_sensormatikskvphysicallocationaccesscardadmitted.md)<br><br> physical_location-access:success(physical-access)<br> ↳[sensormatik-s-cef-physical-location-access-success-sensormatik](Ps/pC_sensormatikscefphysicallocationaccesssuccesssensormatik.md)<br> ↳[sensormatik-s-kv-physical-location-access-cardadmitted](Ps/pC_sensormatikskvphysicallocationaccesscardadmitted.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>3 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_sensormatik_sensormatik_Abnormal_Authentication_&_Access.md) |
|    [Physical Security](../../../UseCases/uc_physical_security.md)    |  physical_location-access:fail(failed-physical-access)<br> ↳[sensormatik-s-cef-physical-location-access-success-sensormatik](Ps/pC_sensormatikscefphysicallocationaccesssuccesssensormatik.md)<br> ↳[sensormatik-s-kv-physical-location-access-cardadmitted](Ps/pC_sensormatikskvphysicallocationaccesscardadmitted.md)<br><br> physical_location-access:success(physical-access)<br> ↳[sensormatik-s-cef-physical-location-access-success-sensormatik](Ps/pC_sensormatikscefphysicallocationaccesssuccesssensormatik.md)<br> ↳[sensormatik-s-kv-physical-location-access-cardadmitted](Ps/pC_sensormatikskvphysicallocationaccesscardadmitted.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>9 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_sensormatik_sensormatik_Physical_Security.md)    |
[Next Page -->>](2_ds_sensormatik_sensormatik.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |