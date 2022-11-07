|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  app-activity<br> ↳[juniper-ps-kv-app-activity-success-webrequestcomplect](Ps/pC_juniperpskvappactivitysuccesswebrequestcomplect.md)<br> ↳[juniper-ps-cef-app-activity-success-requestcompleted](Ps/pC_juniperpscefappactivitysuccessrequestcompleted.md)<br><br> app-activity-failed<br> ↳[juniper-ps-sk4-app-activity-fail-unabletosynctime](Ps/pC_juniperpssk4appactivityfailunabletosynctime.md)<br><br> authentication-successful<br> ↳[juniper-ps-str-vpn-authentication-unauthenticatedrequest](Ps/pC_juniperpsstrvpnauthenticationunauthenticatedrequest.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>39 Rules</li></ul><ul><li>24 Models</li></ul>](RM/r_m_juniper_networks_juniper_pulse_secure_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  app-activity<br> ↳[juniper-ps-kv-app-activity-success-webrequestcomplect](Ps/pC_juniperpskvappactivitysuccesswebrequestcomplect.md)<br> ↳[juniper-ps-cef-app-activity-success-requestcompleted](Ps/pC_juniperpscefappactivitysuccessrequestcompleted.md)<br><br> app-activity-failed<br> ↳[juniper-ps-sk4-app-activity-fail-unabletosynctime](Ps/pC_juniperpssk4appactivityfailunabletosynctime.md)<br><br> authentication-successful<br> ↳[juniper-ps-str-vpn-authentication-unauthenticatedrequest](Ps/pC_juniperpsstrvpnauthenticationunauthenticatedrequest.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>19 Rules</li></ul><ul><li>11 Models</li></ul>](RM/r_m_juniper_networks_juniper_pulse_secure_Data_Access.md)    |
|    [Data Leak](../../../UseCases/uc_data_leak.md)    |  app-activity<br> ↳[juniper-ps-kv-app-activity-success-webrequestcomplect](Ps/pC_juniperpskvappactivitysuccesswebrequestcomplect.md)<br> ↳[juniper-ps-cef-app-activity-success-requestcompleted](Ps/pC_juniperpscefappactivitysuccessrequestcompleted.md)<br><br> app-activity-failed<br> ↳[juniper-ps-sk4-app-activity-fail-unabletosynctime](Ps/pC_juniperpssk4appactivityfailunabletosynctime.md)<br><br> authentication-successful<br> ↳[juniper-ps-str-vpn-authentication-unauthenticatedrequest](Ps/pC_juniperpsstrvpnauthenticationunauthenticatedrequest.md)<br> | T1114.003 - Email Collection: Email Forwarding Rule<br>    | [<ul><li>3 Rules</li></ul>](RM/r_m_juniper_networks_juniper_pulse_secure_Data_Leak.md)    |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  app-activity<br> ↳[juniper-ps-kv-app-activity-success-webrequestcomplect](Ps/pC_juniperpskvappactivitysuccesswebrequestcomplect.md)<br> ↳[juniper-ps-cef-app-activity-success-requestcompleted](Ps/pC_juniperpscefappactivitysuccessrequestcompleted.md)<br><br> app-activity-failed<br> ↳[juniper-ps-sk4-app-activity-fail-unabletosynctime](Ps/pC_juniperpssk4appactivityfailunabletosynctime.md)<br><br> authentication-successful<br> ↳[juniper-ps-str-vpn-authentication-unauthenticatedrequest](Ps/pC_juniperpsstrvpnauthenticationunauthenticatedrequest.md)<br> | T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_juniper_networks_juniper_pulse_secure_Lateral_Movement.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  app-activity<br> ↳[juniper-ps-kv-app-activity-success-webrequestcomplect](Ps/pC_juniperpskvappactivitysuccesswebrequestcomplect.md)<br> ↳[juniper-ps-cef-app-activity-success-requestcompleted](Ps/pC_juniperpscefappactivitysuccessrequestcompleted.md)<br><br> app-activity-failed<br> ↳[juniper-ps-sk4-app-activity-fail-unabletosynctime](Ps/pC_juniperpssk4appactivityfailunabletosynctime.md)<br><br> authentication-successful<br> ↳[juniper-ps-str-vpn-authentication-unauthenticatedrequest](Ps/pC_juniperpsstrvpnauthenticationunauthenticatedrequest.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_juniper_networks_juniper_pulse_secure_Malware.md)    |
|         [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)         |  app-activity<br> ↳[juniper-ps-kv-app-activity-success-webrequestcomplect](Ps/pC_juniperpskvappactivitysuccesswebrequestcomplect.md)<br> ↳[juniper-ps-cef-app-activity-success-requestcompleted](Ps/pC_juniperpscefappactivitysuccessrequestcompleted.md)<br><br> app-activity-failed<br> ↳[juniper-ps-sk4-app-activity-fail-unabletosynctime](Ps/pC_juniperpssk4appactivityfailunabletosynctime.md)<br><br> authentication-successful<br> ↳[juniper-ps-str-vpn-authentication-unauthenticatedrequest](Ps/pC_juniperpsstrvpnauthenticationunauthenticatedrequest.md)<br> | T1078 - Valid Accounts<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br> | [<ul><li>6 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_juniper_networks_juniper_pulse_secure_Privilege_Abuse.md)    |
|    [Privilege Escalation](../../../UseCases/uc_privilege_escalation.md)    |  app-activity<br> ↳[juniper-ps-kv-app-activity-success-webrequestcomplect](Ps/pC_juniperpskvappactivitysuccesswebrequestcomplect.md)<br> ↳[juniper-ps-cef-app-activity-success-requestcompleted](Ps/pC_juniperpscefappactivitysuccessrequestcompleted.md)<br><br> app-activity-failed<br> ↳[juniper-ps-sk4-app-activity-fail-unabletosynctime](Ps/pC_juniperpssk4appactivityfailunabletosynctime.md)<br><br> authentication-successful<br> ↳[juniper-ps-str-vpn-authentication-unauthenticatedrequest](Ps/pC_juniperpsstrvpnauthenticationunauthenticatedrequest.md)<br> | T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>    | [<ul><li>3 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_juniper_networks_juniper_pulse_secure_Privilege_Escalation.md)      |
|     [Privileged Activity](../../../UseCases/uc_privileged_activity.md)     |  app-activity<br> ↳[juniper-ps-kv-app-activity-success-webrequestcomplect](Ps/pC_juniperpskvappactivitysuccesswebrequestcomplect.md)<br> ↳[juniper-ps-cef-app-activity-success-requestcompleted](Ps/pC_juniperpscefappactivitysuccessrequestcompleted.md)<br><br> app-activity-failed<br> ↳[juniper-ps-sk4-app-activity-fail-unabletosynctime](Ps/pC_juniperpssk4appactivityfailunabletosynctime.md)<br><br> authentication-successful<br> ↳[juniper-ps-str-vpn-authentication-unauthenticatedrequest](Ps/pC_juniperpsstrvpnauthenticationunauthenticatedrequest.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_juniper_networks_juniper_pulse_secure_Privileged_Activity.md)       |
|    [Ransomware](../../../UseCases/uc_ransomware.md)    |  app-activity<br> ↳[juniper-ps-kv-app-activity-success-webrequestcomplect](Ps/pC_juniperpskvappactivitysuccesswebrequestcomplect.md)<br> ↳[juniper-ps-cef-app-activity-success-requestcompleted](Ps/pC_juniperpscefappactivitysuccessrequestcompleted.md)<br><br> app-activity-failed<br> ↳[juniper-ps-sk4-app-activity-fail-unabletosynctime](Ps/pC_juniperpssk4appactivityfailunabletosynctime.md)<br><br> authentication-successful<br> ↳[juniper-ps-str-vpn-authentication-unauthenticatedrequest](Ps/pC_juniperpsstrvpnauthenticationunauthenticatedrequest.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_juniper_networks_juniper_pulse_secure_Ransomware.md)    |