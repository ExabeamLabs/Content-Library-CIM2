Rules by Product and UseCase
============================
Vendor: NetMotion Wireless
--------------------------
### Product: [NetMotion Wireless](../ds_netmotion_wireless_netmotion_wireless.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   1    |         2          |       2        |    2    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| vpn-login  | <b>T1078 - Valid Accounts</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account |    |
| vpn-logout | <b>T1078 - Valid Accounts</b><br> ↳ <b>WPA-UACount</b>: Abnormal number of privilege access events for user    |  • <b>WPA-UACount</b>: Count of admin privilege events for user |