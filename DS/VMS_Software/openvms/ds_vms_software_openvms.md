Vendor: VMS Software
====================
Product: OpenVMS
----------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   0    |         1          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Lateral Movement](../../../UseCases/uc_lateral_movement.md) |  logout-remote<br> ↳[vms-openvms-kv-endpoint-logout-success-batchprocesslogout](Ps/pC_vmsopenvmskvendpointlogoutsuccessbatchprocesslogout.md)<br> ↳[vms-openvms-kv-endpoint-logout-success-remoteinteractivelogout](Ps/pC_vmsopenvmskvendpointlogoutsuccessremoteinteractivelogout.md)<br> | T1210 - Exploitation of Remote Services<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_vms_software_openvms_Lateral_Movement.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement                                                                     | Collection | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ------------------------------------------------------------------------------------ | ---------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           | [Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210)<br><br> |            |                     |              |        |