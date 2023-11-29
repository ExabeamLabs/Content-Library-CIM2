Rules by Product and UseCase
============================
Vendor: Cognitas CrossLink
--------------------------
### Product: [Cognitas CrossLink](../ds_cognitas_crosslink_cognitas_crosslink.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   4    |         2          |       1        |    1    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| vpn-login  | <b>T1133 - External Remote Services</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account<br> ↳ <b>AE-UA-F-VPN</b>: First VPN connection for user<br> ↳ <b>AE-GA-F-VPN</b>: First VPN connection for Group<br> ↳ <b>UA-UI-F</b>: First activity from ISP<br> ↳ <b>VPN-GsH-F</b>: First VPN connection from device for peer group<br> ↳ <b>VPN-GsH-A</b>: Abnormal VPN connection from device for peer group<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account<br> ↳ <b>AE-UA-F-VPN</b>: First VPN connection for user<br> ↳ <b>AE-GA-F-VPN</b>: First VPN connection for Group<br> ↳ <b>UA-UI-F</b>: First activity from ISP |  • <b>VPN-GsH</b>: VPN endpoints in this peer group<br> • <b>UA-UI-new</b>: ISP of users during application activity<br> • <b>AE-GA</b>: All activity for peer groups<br> • <b>AE-UA</b>: All activity for users |