Vendor: Proofpoint
==================
Product: Targeted Attack Platform
---------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  72   |   37   |     7      |       5        |    5    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  dlp-alert<br> ↳[proofpoint-tap-cef-email-receive-fail-threat](Ps/pC_proofpointtapcefemailreceivefailthreat.md)<br> ↳[proofpoint-tap-cef-email-receive-fail-threatstatus](Ps/pC_proofpointtapcefemailreceivefailthreatstatus.md)<br> ↳[proofpoint-tap-json-email-receive-fail-threat](Ps/pC_proofpointtapjsonemailreceivefailthreat.md)<br> ↳[proofpoint-tap-cef-alert-trigger-success-proofpoint](Ps/pC_proofpointtapcefalerttriggersuccessproofpoint.md)<br> ↳[proofpoint-pep-cef-email-alert-success-emaildelivery](Ps/pC_proofpointpepcefemailalertsuccessemaildelivery.md)<br> ↳[proofpoint-tap-json-email-receive-emailthreat-1](Ps/pC_proofpointtapjsonemailreceiveemailthreat1.md)<br><br> dlp-email-alert-in<br> ↳[proofpoint-tap-json-email-envelope](Ps/pC_proofpointtapjsonemailenvelope.md)<br> ↳[proofpoint-tap-json-email-emailthreat](Ps/pC_proofpointtapjsonemailemailthreat.md)<br> ↳[proofpoint-tap-kv-email-receive-mailreceived](Ps/pC_proofpointtapkvemailreceivemailreceived.md)<br> ↳[proofpoint-tap-json-email-receive-emailthreat-1](Ps/pC_proofpointtapjsonemailreceiveemailthreat1.md)<br> ↳[proofpoint-tap-sk4-email-routedirection](Ps/pC_proofpointtapsk4emailroutedirection.md)<br><br> dlp-email-alert-in-failed<br> ↳[proofpoint-tap-cef-email-receive-fail-threat](Ps/pC_proofpointtapcefemailreceivefailthreat.md)<br> ↳[proofpoint-tap-cef-email-receive-fail-threatstatus](Ps/pC_proofpointtapcefemailreceivefailthreatstatus.md)<br> ↳[proofpoint-tap-leef-email-receive-fail-threatinsight](Ps/pC_proofpointtapleefemailreceivefailthreatinsight.md)<br> ↳[proofpoint-tap-json-email-receive-fail-threat](Ps/pC_proofpointtapjsonemailreceivefailthreat.md)<br> ↳[proofpoint-tap-json-email-envelope](Ps/pC_proofpointtapjsonemailenvelope.md)<br> ↳[proofpoint-tap-json-email-emailthreat](Ps/pC_proofpointtapjsonemailemailthreat.md)<br> ↳[proofpoint-tap-kv-email-receive-mailreceived](Ps/pC_proofpointtapkvemailreceivemailreceived.md)<br> ↳[proofpoint-tap-json-email-receive-emailthreat-1](Ps/pC_proofpointtapjsonemailreceiveemailthreat1.md)<br> ↳[proofpoint-tap-sk4-email-routedirection](Ps/pC_proofpointtapsk4emailroutedirection.md)<br><br> dlp-email-alert-out<br> ↳[proofpoint-tap-json-email-envelope](Ps/pC_proofpointtapjsonemailenvelope.md)<br> ↳[proofpoint-pep-cef-email-alert-success-emaildelivery](Ps/pC_proofpointpepcefemailalertsuccessemaildelivery.md)<br> ↳[proofpoint-tap-json-email-emailthreat](Ps/pC_proofpointtapjsonemailemailthreat.md)<br> ↳[proofpoint-tap-sk4-email-routedirection](Ps/pC_proofpointtapsk4emailroutedirection.md)<br><br> dlp-email-alert-out-failed<br> ↳[proofpoint-tap-json-email-envelope](Ps/pC_proofpointtapjsonemailenvelope.md)<br> ↳[proofpoint-tap-json-email-emailthreat](Ps/pC_proofpointtapjsonemailemailthreat.md)<br> ↳[proofpoint-tap-sk4-email-routedirection](Ps/pC_proofpointtapsk4emailroutedirection.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br>    | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_proofpoint_targeted_attack_platform_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  dlp-alert<br> ↳[proofpoint-tap-cef-email-receive-fail-threat](Ps/pC_proofpointtapcefemailreceivefailthreat.md)<br> ↳[proofpoint-tap-cef-email-receive-fail-threatstatus](Ps/pC_proofpointtapcefemailreceivefailthreatstatus.md)<br> ↳[proofpoint-tap-json-email-receive-fail-threat](Ps/pC_proofpointtapjsonemailreceivefailthreat.md)<br> ↳[proofpoint-tap-cef-alert-trigger-success-proofpoint](Ps/pC_proofpointtapcefalerttriggersuccessproofpoint.md)<br> ↳[proofpoint-pep-cef-email-alert-success-emaildelivery](Ps/pC_proofpointpepcefemailalertsuccessemaildelivery.md)<br> ↳[proofpoint-tap-json-email-receive-emailthreat-1](Ps/pC_proofpointtapjsonemailreceiveemailthreat1.md)<br><br> dlp-email-alert-in<br> ↳[proofpoint-tap-json-email-envelope](Ps/pC_proofpointtapjsonemailenvelope.md)<br> ↳[proofpoint-tap-json-email-emailthreat](Ps/pC_proofpointtapjsonemailemailthreat.md)<br> ↳[proofpoint-tap-kv-email-receive-mailreceived](Ps/pC_proofpointtapkvemailreceivemailreceived.md)<br> ↳[proofpoint-tap-json-email-receive-emailthreat-1](Ps/pC_proofpointtapjsonemailreceiveemailthreat1.md)<br> ↳[proofpoint-tap-sk4-email-routedirection](Ps/pC_proofpointtapsk4emailroutedirection.md)<br><br> dlp-email-alert-in-failed<br> ↳[proofpoint-tap-cef-email-receive-fail-threat](Ps/pC_proofpointtapcefemailreceivefailthreat.md)<br> ↳[proofpoint-tap-cef-email-receive-fail-threatstatus](Ps/pC_proofpointtapcefemailreceivefailthreatstatus.md)<br> ↳[proofpoint-tap-leef-email-receive-fail-threatinsight](Ps/pC_proofpointtapleefemailreceivefailthreatinsight.md)<br> ↳[proofpoint-tap-json-email-receive-fail-threat](Ps/pC_proofpointtapjsonemailreceivefailthreat.md)<br> ↳[proofpoint-tap-json-email-envelope](Ps/pC_proofpointtapjsonemailenvelope.md)<br> ↳[proofpoint-tap-json-email-emailthreat](Ps/pC_proofpointtapjsonemailemailthreat.md)<br> ↳[proofpoint-tap-kv-email-receive-mailreceived](Ps/pC_proofpointtapkvemailreceivemailreceived.md)<br> ↳[proofpoint-tap-json-email-receive-emailthreat-1](Ps/pC_proofpointtapjsonemailreceiveemailthreat1.md)<br> ↳[proofpoint-tap-sk4-email-routedirection](Ps/pC_proofpointtapsk4emailroutedirection.md)<br><br> dlp-email-alert-out<br> ↳[proofpoint-tap-json-email-envelope](Ps/pC_proofpointtapjsonemailenvelope.md)<br> ↳[proofpoint-pep-cef-email-alert-success-emaildelivery](Ps/pC_proofpointpepcefemailalertsuccessemaildelivery.md)<br> ↳[proofpoint-tap-json-email-emailthreat](Ps/pC_proofpointtapjsonemailemailthreat.md)<br> ↳[proofpoint-tap-sk4-email-routedirection](Ps/pC_proofpointtapsk4emailroutedirection.md)<br><br> dlp-email-alert-out-failed<br> ↳[proofpoint-tap-json-email-envelope](Ps/pC_proofpointtapjsonemailenvelope.md)<br> ↳[proofpoint-tap-json-email-emailthreat](Ps/pC_proofpointtapjsonemailemailthreat.md)<br> ↳[proofpoint-tap-sk4-email-routedirection](Ps/pC_proofpointtapsk4emailroutedirection.md)<br> | T1020 - Automated Exfiltration<br>T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>63 Rules</li></ul><ul><li>34 Models</li></ul>](RM/r_m_proofpoint_targeted_attack_platform_Data_Leak.md)         |
[Next Page -->>](2_ds_proofpoint_targeted_attack_platform.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                            | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                                                                                                                                                                                                                                                                    | Impact |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048)<br><br>[Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol](https://attack.mitre.org/techniques/T1048/003)<br><br>[Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |