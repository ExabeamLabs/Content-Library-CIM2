Rules by Product and UseCase
============================
Vendor: Avaya
-------------
### Product: [Avaya VPN](../ds_avaya_avaya_vpn.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   7   |   4    |         2          |       1        |    1    |

| Event Type       | Rules    | Models    |
| ---- | ---- | ---- |
| failed-vpn-login | <b>T1133 - External Remote Services</b><br> ↳ <b>SEQ-UH-15</b>: Failed VPN login    |    |
| vpn-login        | <b>T1133 - External Remote Services</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account<br> ↳ <b>AE-UA-F-VPN</b>: First VPN connection for user<br> ↳ <b>AE-GA-F-VPN</b>: First VPN connection for Group<br> ↳ <b>UA-UI-F</b>: First activity from ISP<br> ↳ <b>VPN-GsH-F</b>: First VPN connection from device for peer group<br> ↳ <b>VPN-GsH-A</b>: Abnormal VPN connection from device for peer group<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account<br> ↳ <b>AE-UA-F-VPN</b>: First VPN connection for user<br> ↳ <b>AE-GA-F-VPN</b>: First VPN connection for Group<br> ↳ <b>UA-UI-F</b>: First activity from ISP |  • <b>VPN-GsH</b>: VPN endpoints in this peer group<br> • <b>UA-UI-new</b>: ISP of users during application activity<br> • <b>AE-GA</b>: All activity for peer groups<br> • <b>AE-UA</b>: All activity for users |