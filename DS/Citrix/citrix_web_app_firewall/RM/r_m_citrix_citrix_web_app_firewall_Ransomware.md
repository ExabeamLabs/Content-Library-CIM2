Rules by Product and UseCase
============================
Vendor: Citrix
--------------
### Product: [Citrix Web App Firewall](../ds_citrix_citrix_web_app_firewall.md)
### Use-Case: [Ransomware](../../../../UseCases/uc_ransomware.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   0    |         3          |       4        |   14    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| authentication-successful     | <b>T1078 - Valid Accounts</b><br> ↳ <b>Auth-Ransomware-Shost</b>: User authentication or login from a known ransomware IP    |        |
| network-connection-failed     | <b>TA0011 - TA0011</b><br> ↳ <b>A-NETF-Ransomware-IP</b>: Asset failed to connect to an IP address which is associated to Ransomware    |        |
| network-connection-successful | <b>TA0011 - TA0011</b><br> ↳ <b>A-NET-Ransomware-IP</b>: Asset attempted to connect to an IP address which is associated to Ransomware    |        |
| web-activity-allowed          | <b>TA0011 - TA0011</b><br> ↳ <b>A-NET-Ransomware-IP</b>: Asset attempted to connect to an IP address which is associated to Ransomware<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-UI-Ransomware</b>: User attempted to connect to IP address which is associated to Ransomware<br> ↳ <b>WEB-UD-Ransomware</b>: User attempted to connect to domain which is associated to Ransomware<br> ↳ <b>A-WEB-Ransomware-Domain</b>: Asset attempted to connect to domain which is associated to Ransomware |        |