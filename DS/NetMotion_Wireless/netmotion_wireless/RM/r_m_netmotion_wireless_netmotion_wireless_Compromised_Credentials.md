Rules by Product and UseCase
============================
Vendor: NetMotion Wireless
--------------------------
### Product: [NetMotion Wireless](../ds_netmotion_wireless_netmotion_wireless.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  13   |   7    |         2          |       3        |    3    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| authentication-successful | <b>T1078 - Valid Accounts</b><br> ↳ <b>UA-UI-F</b>: First activity from ISP<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>UA-UI-F</b>: First activity from ISP    |  • <b>UA-UI-new</b>: ISP of users during application activity    |
| vpn-login    | <b>T1133 - External Remote Services</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account<br> ↳ <b>AE-UA-F-VPN</b>: First VPN connection for user<br> ↳ <b>AE-GA-F-VPN</b>: First VPN connection for Group<br> ↳ <b>UA-UI-F</b>: First activity from ISP<br> ↳ <b>VPN-GsH-F</b>: First VPN connection from device for peer group<br> ↳ <b>VPN-GsH-A</b>: Abnormal VPN connection from device for peer group<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account<br> ↳ <b>AE-UA-F-VPN</b>: First VPN connection for user<br> ↳ <b>AE-GA-F-VPN</b>: First VPN connection for Group<br> ↳ <b>UA-UI-F</b>: First activity from ISP |  • <b>VPN-GsH</b>: VPN endpoints in this peer group<br> • <b>UA-UI-new</b>: ISP of users during application activity<br> • <b>AE-GA</b>: All activity for peer groups<br> • <b>AE-UA</b>: All activity for users |
| vpn-logout    | <b>T1078 - Valid Accounts</b><br> ↳ <b>AL-UHcount-S</b>: Abnormal number of logon assets (S)<br> ↳ <b>AL-UHcount-M</b>: Abnormal number of logon assets (M)<br> ↳ <b>AL-UHcount-L</b>: Abnormal number of logon assets (L)<br> ↳ <b>AL-OHcount</b>: Abnormal number of logged on assets compared to the organization<br> ↳ <b>AL-GHcount</b>: Abnormal number of logged on assets compared to group<br> ↳ <b>VPN-End-DUR</b>: Abnormal VPN session duration<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>VPN-BSum</b>: Abnormal amount of data uploaded during VPN Session<br> ↳ <b>VPN-End-DUR</b>: Abnormal VPN session duration    |  • <b>VPN-End-DUR</b>: VPN session duration<br> • <b>VPN-BSum</b>: Sum of bytes uploaded during VPN<br> • <b>AL-OHcount</b>: Count of assets logon per user in the organization    |