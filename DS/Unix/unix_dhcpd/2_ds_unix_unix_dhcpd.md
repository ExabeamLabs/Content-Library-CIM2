|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  app-login<br> ↳[unix-unixdhcpd-str-endpoint-notification-parameter](Ps/pC_unixunixdhcpdstrendpointnotificationparameter.md)<br><br> authentication-successful<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpd](Ps/pC_unixdhcpdstrdhcptrafficdhcpd.md)<br> ↳[unix-dhcpd-csv-dhcp-traffic-release](Ps/pC_unixdhcpdcsvdhcptrafficrelease.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpnak](Ps/pC_unixdhcpdstrdhcptrafficdhcpnak.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcprelease](Ps/pC_unixdhcpdstrdhcptrafficdhcprelease.md)<br> ↳[unix-dhcpd-csv-dhcp-traffic-expired](Ps/pC_unixdhcpdcsvdhcptrafficexpired.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpinform](Ps/pC_unixdhcpdstrdhcptrafficdhcpinform.md)<br>    | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>T1190 - Exploit Public Fasing Application<br> | [<ul><li>27 Rules</li></ul><ul><li>16 Models</li></ul>](RM/r_m_unix_unix_dhcpd_Compromised_Credentials.md) |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  app-login<br> ↳[unix-unixdhcpd-str-endpoint-notification-parameter](Ps/pC_unixunixdhcpdstrendpointnotificationparameter.md)<br><br> authentication-successful<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpd](Ps/pC_unixdhcpdstrdhcptrafficdhcpd.md)<br> ↳[unix-dhcpd-csv-dhcp-traffic-release](Ps/pC_unixdhcpdcsvdhcptrafficrelease.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpnak](Ps/pC_unixdhcpdstrdhcptrafficdhcpnak.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcprelease](Ps/pC_unixdhcpdstrdhcptrafficdhcprelease.md)<br> ↳[unix-dhcpd-csv-dhcp-traffic-expired](Ps/pC_unixdhcpdcsvdhcptrafficexpired.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpinform](Ps/pC_unixdhcpdstrdhcptrafficdhcpinform.md)<br>    | T1090.003 - Proxy: Multi-hop Proxy<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_unix_unix_dhcpd_Lateral_Movement.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  app-login<br> ↳[unix-unixdhcpd-str-endpoint-notification-parameter](Ps/pC_unixunixdhcpdstrendpointnotificationparameter.md)<br><br> authentication-successful<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpd](Ps/pC_unixdhcpdstrdhcptrafficdhcpd.md)<br> ↳[unix-dhcpd-csv-dhcp-traffic-release](Ps/pC_unixdhcpdcsvdhcptrafficrelease.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpnak](Ps/pC_unixdhcpdstrdhcptrafficdhcpnak.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcprelease](Ps/pC_unixdhcpdstrdhcptrafficdhcprelease.md)<br> ↳[unix-dhcpd-csv-dhcp-traffic-expired](Ps/pC_unixdhcpdcsvdhcptrafficexpired.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpinform](Ps/pC_unixdhcpdstrdhcptrafficdhcpinform.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_unix_unix_dhcpd_Malware.md)    |
|         [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)         |  account-password-change<br> ↳[unix-dhcpd-str-dhcp-discoverdhcpd](Ps/pC_unixdhcpdstrdhcpdiscoverdhcpd.md)<br> ↳[unix-dhcpd-str-dhcp-discover-nofreeleases](Ps/pC_unixdhcpdstrdhcpdiscovernofreeleases.md)<br> ↳[unix-dhcpd-csv-dns-record-delete-fail-notdeleted](Ps/pC_unixdhcpdcsvdnsrecorddeletefailnotdeleted.md)<br> ↳[unix-dhcpd-str-dhcp-acknowledge-dhcpack](Ps/pC_unixdhcpdstrdhcpacknowledgedhcpack.md)<br> ↳[unix-dhcpd-str-app-notification-balancingpool](Ps/pC_unixdhcpdstrappnotificationbalancingpool.md)<br> ↳[unix-dhcpd-str-app-notification-reuselease](Ps/pC_unixdhcpdstrappnotificationreuselease.md)<br> ↳[unix-dhcpd-str-app-notification-balancedpool](Ps/pC_unixdhcpdstrappnotificationbalancedpool.md)<br><br> app-login<br> ↳[unix-unixdhcpd-str-endpoint-notification-parameter](Ps/pC_unixunixdhcpdstrendpointnotificationparameter.md)<br> | T1078 - Valid Accounts<br>T1098 - Account Manipulation<br>    | [<ul><li>3 Rules</li></ul>](RM/r_m_unix_unix_dhcpd_Privilege_Abuse.md)    |
|    [Ransomware](../../../UseCases/uc_ransomware.md)    |  app-login<br> ↳[unix-unixdhcpd-str-endpoint-notification-parameter](Ps/pC_unixunixdhcpdstrendpointnotificationparameter.md)<br><br> authentication-successful<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpd](Ps/pC_unixdhcpdstrdhcptrafficdhcpd.md)<br> ↳[unix-dhcpd-csv-dhcp-traffic-release](Ps/pC_unixdhcpdcsvdhcptrafficrelease.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpnak](Ps/pC_unixdhcpdstrdhcptrafficdhcpnak.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcprelease](Ps/pC_unixdhcpdstrdhcptrafficdhcprelease.md)<br> ↳[unix-dhcpd-csv-dhcp-traffic-expired](Ps/pC_unixdhcpdcsvdhcptrafficexpired.md)<br> ↳[unix-dhcpd-str-dhcp-traffic-dhcpinform](Ps/pC_unixdhcpdstrdhcptrafficdhcpinform.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_unix_unix_dhcpd_Ransomware.md)    |