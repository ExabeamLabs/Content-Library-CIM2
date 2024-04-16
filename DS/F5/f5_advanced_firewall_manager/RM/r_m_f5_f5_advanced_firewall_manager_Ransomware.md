Rules by Product and UseCase
============================
Vendor: F5
----------
### Product: [F5 Advanced Firewall Manager](../ds_f5_f5_advanced_firewall_manager.md)
### Use-Case: [Ransomware](../../../../UseCases/uc_ransomware.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         2          |       3        |    1    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| authentication-failed         | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost-Failed</b>: User authentication or login failure from a known ransomware IP |        |
| network-connection-failed     | <b>TA0011 - TA0011</b><br> ↳ <b>A-NETF-Ransomware-IP</b>: Asset failed to connect to an IP address which is associated to Ransomware     |        |
| network-connection-successful | <b>TA0011 - TA0011</b><br> ↳ <b>A-NET-Ransomware-IP</b>: Asset attempted to connect to an IP address which is associated to Ransomware   |        |