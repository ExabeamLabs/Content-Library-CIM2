|    Use-Case    | Activity Type (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  scheduled_task-trigger:success (app-activity)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br><br> network-traffic:success (netflow-connection)<br> ↳[fortinet-firewall-json-network-traffic-success-trafficlocality](Ps/pC_fortinetfirewalljsonnetworktrafficsuccesstrafficlocality.md)<br><br> http-traffic:success (web-activity-allowed)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br><br> http-session:fail (web-activity-denied)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br>    | T1046 - Network Service Scanning<br>T1071 - Application Layer Protocol<br>T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>T1102 - Web Service<br>T1133 - External Remote Services<br>T1189 - Drive-by Compromise<br>T1190 - Exploit Public Fasing Application<br>T1204 - User Execution<br>T1204.001 - T1204.001<br>T1566 - Phishing<br>T1566.002 - Phishing: Spearphishing Link<br>T1568 - Dynamic Resolution<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br> | [<ul><li>80 Rules</li></ul><ul><li>47 Models</li></ul>](RM/r_m_fortinet_fortinet_enterprise_firewall_Compromised_Credentials.md) |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  network-traffic:success (netflow-connection)<br> ↳[fortinet-firewall-json-network-traffic-success-trafficlocality](Ps/pC_fortinetfirewalljsonnetworktrafficsuccesstrafficlocality.md)<br><br> network-traffic:fail (network-connection-failed)<br> ↳[fortinet-firewall-kv-network-traffic-fail-traffic](Ps/pC_fortinetfirewallkvnetworktrafficfailtraffic.md)<br> ↳[fortinet-firewall-str-network-traffic-fail-deny](Ps/pC_fortinetfirewallstrnetworktrafficfaildeny.md)<br> ↳[fortinet-firewall-str-network-traffic-fail-deny-1](Ps/pC_fortinetfirewallstrnetworktrafficfaildeny1.md)<br> ↳[fortinet-firewall-cef-network-traffic-connectionaction](Ps/pC_fortinetfirewallcefnetworktrafficconnectionaction.md)<br> ↳[fortinet-firewall-kv-network-traffic-notice](Ps/pC_fortinetfirewallkvnetworktrafficnotice.md)<br> ↳[fortinet-firewall-str-network-close-success-teardownconnection](Ps/pC_fortinetfirewallstrnetworkclosesuccessteardownconnection.md)<br> ↳[fortinet-firewall-str-network-close-success-teardown](Ps/pC_fortinetfirewallstrnetworkclosesuccessteardown.md)<br><br> network-traffic:success (network-connection-successful)<br> ↳[fortinet-firewall-kv-network-traffic-success-accept](Ps/pC_fortinetfirewallkvnetworktrafficsuccessaccept.md)<br> ↳[fortinet-firewall-cef-network-traffic-connectionaction](Ps/pC_fortinetfirewallcefnetworktrafficconnectionaction.md)<br> ↳[fortinet-firewall-kv-network-traffic-notice](Ps/pC_fortinetfirewallkvnetworktrafficnotice.md)<br> ↳[fortinet-firewall-kv-network-traffic-notice](Ps/pC_fortinetfirewallkvnetworktrafficnotice.md)<br> ↳[fortinet-firewall-str-network-start-success-builtdynamic](Ps/pC_fortinetfirewallstrnetworkstartsuccessbuiltdynamic.md)<br> ↳[fortinet-firewall-str-network-start-success-built](Ps/pC_fortinetfirewallstrnetworkstartsuccessbuilt.md)<br><br> http-traffic:success (web-activity-allowed)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br><br> http-session:fail (web-activity-denied)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br> | T1018 - Remote System Discovery<br>T1021 - Remote Services<br>T1021.001 - Remote Services: Remote Desktop Protocol<br>T1046 - Network Service Scanning<br>T1071 - Application Layer Protocol<br>T1071.001 - Application Layer Protocol: Web Protocols<br>T1090 - Proxy<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1190 - Exploit Public Fasing Application<br>T1210 - Exploitation of Remote Services<br>TA0008 - TA0008<br>TA0010 - TA0010<br>TA0011 - TA0011<br>    | [<ul><li>79 Rules</li></ul><ul><li>27 Models</li></ul>](RM/r_m_fortinet_fortinet_enterprise_firewall_Lateral_Movement.md)        |
|    [Malware](../../../UseCases/uc_malware.md)    |  network-traffic:success (netflow-connection)<br> ↳[fortinet-firewall-json-network-traffic-success-trafficlocality](Ps/pC_fortinetfirewalljsonnetworktrafficsuccesstrafficlocality.md)<br><br> network-traffic:fail (network-connection-failed)<br> ↳[fortinet-firewall-kv-network-traffic-fail-traffic](Ps/pC_fortinetfirewallkvnetworktrafficfailtraffic.md)<br> ↳[fortinet-firewall-str-network-traffic-fail-deny](Ps/pC_fortinetfirewallstrnetworktrafficfaildeny.md)<br> ↳[fortinet-firewall-str-network-traffic-fail-deny-1](Ps/pC_fortinetfirewallstrnetworktrafficfaildeny1.md)<br> ↳[fortinet-firewall-cef-network-traffic-connectionaction](Ps/pC_fortinetfirewallcefnetworktrafficconnectionaction.md)<br> ↳[fortinet-firewall-kv-network-traffic-notice](Ps/pC_fortinetfirewallkvnetworktrafficnotice.md)<br> ↳[fortinet-firewall-str-network-close-success-teardownconnection](Ps/pC_fortinetfirewallstrnetworkclosesuccessteardownconnection.md)<br> ↳[fortinet-firewall-str-network-close-success-teardown](Ps/pC_fortinetfirewallstrnetworkclosesuccessteardown.md)<br><br> network-traffic:success (network-connection-successful)<br> ↳[fortinet-firewall-kv-network-traffic-success-accept](Ps/pC_fortinetfirewallkvnetworktrafficsuccessaccept.md)<br> ↳[fortinet-firewall-cef-network-traffic-connectionaction](Ps/pC_fortinetfirewallcefnetworktrafficconnectionaction.md)<br> ↳[fortinet-firewall-kv-network-traffic-notice](Ps/pC_fortinetfirewallkvnetworktrafficnotice.md)<br> ↳[fortinet-firewall-kv-network-traffic-notice](Ps/pC_fortinetfirewallkvnetworktrafficnotice.md)<br> ↳[fortinet-firewall-str-network-start-success-builtdynamic](Ps/pC_fortinetfirewallstrnetworkstartsuccessbuiltdynamic.md)<br> ↳[fortinet-firewall-str-network-start-success-built](Ps/pC_fortinetfirewallstrnetworkstartsuccessbuilt.md)<br><br> http-traffic:success (web-activity-allowed)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br><br> http-session:fail (web-activity-denied)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br> | T1071 - Application Layer Protocol<br>T1071.001 - Application Layer Protocol: Web Protocols<br>T1189 - Drive-by Compromise<br>T1190 - Exploit Public Fasing Application<br>T1204 - User Execution<br>T1204.001 - T1204.001<br>T1566 - Phishing<br>T1566.002 - Phishing: Spearphishing Link<br>T1568 - Dynamic Resolution<br>T1568.002 - Dynamic Resolution: Domain Generation Algorithms<br>TA0011 - TA0011<br>    | [<ul><li>29 Rules</li></ul><ul><li>7 Models</li></ul>](RM/r_m_fortinet_fortinet_enterprise_firewall_Malware.md)    |
|         [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)         |  scheduled_task-trigger:success (app-activity)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br><br> app-activity:fail (app-activity-failed)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br><br> http-traffic:success (web-activity-allowed)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br><br> http-session:fail (web-activity-denied)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br>    | T1071 - Application Layer Protocol<br>T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>T1098 - Account Manipulation<br>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions<br>    | [<ul><li>7 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_fortinet_fortinet_enterprise_firewall_Privilege_Abuse.md)    |
|     [Privileged Activity](../../../UseCases/uc_privileged_activity.md)     |  scheduled_task-trigger:success (app-activity)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br><br> app-activity:fail (app-activity-failed)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br><br> http-traffic:success (web-activity-allowed)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br><br> http-session:fail (web-activity-denied)<br> ↳[fortinet-firewall-cef-app-activity-appctrl](Ps/pC_fortinetfirewallcefappactivityappctrl.md)<br>    | T1071 - Application Layer Protocol<br>T1071.001 - Application Layer Protocol: Web Protocols<br>T1078 - Valid Accounts<br>T1102 - Web Service<br>    | [<ul><li>4 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_fortinet_fortinet_enterprise_firewall_Privileged_Activity.md)       |